## Useful SSH commands

### Generating new SSH keys
```bash
ssh-keygen -t rsa 
```

### Add ssh-key to ssh-agent
```bash
# ensure that the ssh-agent program is running
eval $(ssh-agent -s)
```

Now add the ssh-key to agent
```bash
ssh-add ~/.ssh/id_rsa
```


### Add public key to remote server for key-based authentication
```bash
ssh-copy-id username@remote_server_ip
```

OR

```bash
cat ~/.ssh/id_rsa.pub | ssh username@remote_server_ip "mkdir -p ~/.ssh && cat >>  ~/.ssh/authorized_keys"
```
