# git-task

The following code installs the Open-SSH Client on linux. However, most operating systems comes pre-installed with OpenSSH.
OpenSSH comes pre-installed on Windows 10 and above.

```bash
sudo apt install openssh-client 
```

The following code generates an SSH key:

```bash
ssh-keygen -t ed25519 -C "yourexample@email.com"
```

The terminal will prompt:
```bash
Enter file in which to save the key (/home/your_user/.ssh/id_ed25519):
```
The terminal will then ask for:
```bash
Enter passphrase (empty for no passphrase):
```

This code adds the generated key to the SSH agent and displays the key. Copy the key. 
```bash
eval "$(ssh-agent -s)"
ssh-add ~/.ssh/id_ed25519
cat ~/.ssh/id_ed25519.pub
```

Go to Github > Settings > SSH and GPG keys > New SSH key.
Give a name of your choice, paste the copied key and save.

Your SSH Public key is now authorized with GitHub and is ready to use.
