# Authenticating with SSH key pairs

  The following step-by-step tutorial will allow you to log in to an SSH server with a public-private key pair and use MacOS Keychain to store the passphrase

* **On your local machine**, generate a key pair:
  ```bash
  ssh-keygen -f ~/.ssh/computecanada
  ```
   **Do not leave the passphrase empty**. You'll only need to re-enter it once after the key is generated, so memorizing it long-term is not important. If you use a password manager, you can auto-generate one and store it as a password item.


* You can use the SSH Authentication Agent to remember passphrases for keys. On MacOS, the `-K` option will also add the key's passphrase to MacOS Keychain, so don't have to re-enter it every time the agent is started/restarted (user logout, system reboot, etc). (**`-K` only works on MacOS!**):
  ```bash
  ssh-add -K ~/.ssh/computecanada
  ```
  If the command returns `Error connecting to agent: No such file or directory`, you need to launch an `ssh-agent` before-running `ssh-add`:
  ```
  eval $(ssh-agent -s)
  ssh-add -K ~/.ssh/computecanada
  ```

* To avoid having to run the above step manually each time you launch a new Terminal window, add the following into your `~/.bash_profile`:
  
  ```bash
  # Add this line to local ~/.bash_profile
  ssh-add -q -A
  ```
  
  This will try adding all ssh keys to the agent, and if there's a failure it will launch the agent and try again.
  
  Or you can limit it to one specific key by specifying it instead of the `-A` option:
  
  ```bash
  # Add this line to local ~/.bash_profile
  ssh-add -q -K ~/.ssh/computecanada
  ```

* Now you can transfer the public key over to the home directory of the remote user on a remote server, which will authorize you to log in using the private key:

  ```bash
  ssh-copy-id -i ~/.ssh/computecanada isolovey@graham.computecanada.ca
  ```
  
  This will prompt you for the password of `isolovey@graham.computecanada.ca`.

* By default, `ssh` will try every key on every server you log in to, until it finds one that works. SSH servers usually set limits on how many login attempts are allowed before your access is denied, so it's a good idea to tell your SSH client to always use the key you just generated on e.g. all Compute Canada servers. Append to `~/.ssh/config`:

   ```
  # Add this line to local ~/.ssh/config:
  Host *.computecanada.ca
    User isolovey
    IdentityFile ~/.ssh/computecanada
  ```
  
  Specifying the user here allows you to omit it when running the `ssh` command later on.

  
* To test that everything worked, restart your Terminal app and try to log in:

  ```bash
  ssh graham.computecanada.ca
  ```
  
  ## Troubleshooting
  
  1. On Compute Canada servers, the above will not work unless `group` and `other` have no read, write or execute permissions on your home directory. Run the following on a Compute Canada server to make sure:
  
  ```bash
  chmod go-rwx $HOME
  ```
