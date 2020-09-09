# Add New Computer SSH key to Github

```
ssh-keygen -t rsa -b 4096 -C "your_email@example.com"
# hit enter a bunch

# add the key to the SSH agent
eval $(ssh-agent -s) 
ssh-add ~/.ssh/id_rsa

# copy the key
vim ~/.ssh/id_rsa.pub 
```

Copy and then add the new key to Github here: https://github.com/settings/keys
