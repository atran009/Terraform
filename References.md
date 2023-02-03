#Connect local machine to Github account
**Generate SSH keys**
-Command to generate SSH key, type of encryption, strength of encryption, and email to connect it to
ssh-keygen -t rsa -b 4096 -C "emailaddress"
-ls to list your files after your key is created
-cat the .pub key 
-Add .pub key to github account

**Check connection**
-Start the ssh-agent in the background
eval $(ssh-agent -s)
-Add your SSH key to the ssh-agent
ssh-add ~locationofprivatekeyfile 
ex: ssh-add ~./ssh/id_rsa
-Check connection
ssh -T git@github.com
