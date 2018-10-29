# ssh (and other related commands)

**Generate ssh key**
```bash
ssh-keygen -o -a 100 -t ed25519
```

**Force password authentication**:
```bash
ssh -o PreferredAuthentications=password -o PubkeyAuthentication=no example.com
```

**Search for a server line in known_hosts**:
```bash
ssh-keygen -l -F SERVER
```

**Ignore new key warning:**
```bash
ssh -o UserKnownHostsFile=/dev/null -o StrictHostKeyChecking=no user@IP
```
