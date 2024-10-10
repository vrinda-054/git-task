# git-task



```bash
sudo apt install openssh-client 
```

generate ssh keys 

```bash
ssh-keygen -t ed25519 -C "yourexample@email.com"
```

The terminal will prompt:
```bash
Enter file in which to save the key (/home/your_user/.ssh/id_ed25519):
```
it will then ask for:
```bash
Enter passphrase (empty for no passphrase):
```

```bash
eval "$(ssh-agent -s)"
ssh-add ~/.ssh/id_ed25519
cat ~/.ssh/id_ed25519.pub
```
copy the output (ssh key) and 
go to github > settings > SSH and GPG keys > New SSH key and paste it 
