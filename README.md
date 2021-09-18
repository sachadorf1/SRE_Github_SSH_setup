# SSH setup between our Localhost and Github
## Generating SSH keys
- On localhost, go into your .ssh folder
`cd .ssh`
- To generate a public/private rsa key pair enter `ssh-keygen -t rsa -b 4096 -C "your email address"` using the email address for your Github account
- Enter file in which to save the key: Name the key pair or press enter and it will be named id_rsa (and id_rsa.pub)
- Press enter to the other questions
- You should see your key pair (e.g. id_rsa and id_rsa.pub) in your .ssh folder when you `ls`
- id_rsa is your private key
- id_rsa.pub is your public key
- `cat id_rsa.pub` and copy the results (should start with ssh-rsa ... and end with the email address for your Github)
## Deploying SSH keys to Github
- In Github, go into your settings
- Click on `SSH and GPG keys` on the side tab
- Click `New SSH key`
- Title: Give your key a descriptive title (e.g. SRE_CICD)
- Key: Paste the results you copied from your public key in previous section (with `cat id_rsa.pub`)
- Click `Add SSH key`
