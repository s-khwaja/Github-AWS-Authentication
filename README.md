# Github AWS Authentication

1. Log in to AWS EC2 (Ubuntu)

ssh-keygen -t ed25519

cd ~/.ssh/

eval "$(ssh-agent -s)"

nano config

  Host *
    AddKeysToAgent yes
    IdentifyFile ~/.ssh/id_ed25519
    
 ssh-add ~/.ssh/id_ed25519
    
 2. Now copy and the .pub key that was just generated and paste it into Github
 
 cat ~/.ssh/config
 
 3. To test the connection
 
 ssh -T git@github.com
 
