# How to Use Git Guide

- This is a guide for commands to remind myself how to use Github 

----

### How to setup ssh key

1️⃣ **Generate a new SSH key**
```bash
ssh-keygen -t ed25519 -C "YOUR_EMAIL_FOR_HERE"
```

2️⃣ **Start the SSH agent and add your key**
```bash
eval "$(ssh-agent -s)"
ssh-add ~/.ssh/id_ed25519
```

3️⃣ **Copy your SSH public key**
```bash
clip < ~/.ssh/id_ed25519.pub
```

4️⃣ **Add the key to GitHub**
```bash
- Go to: https://github.com/settings/keys
- Click New SSH Key
- Title: "DESKTOP-N4US1BD" (or anything meaningful)
- Paste the key (copied in step 3)
- Save
```

5️⃣ **Test the connection**
```bash
ssh -T git@github.com
```
- Will recieve: Hi dboieng! You've successfully authenticated, but GitHub does not provide shell access.

6️⃣ **Clone the repo using SSH**
```bash
git clone git@github.com:dboieng/Finance.git
```
