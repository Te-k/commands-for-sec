# fail2ban

**Check enabled jails:**
```
sudo fail2ban-client status
```

**Check actions on a jail:**
```
sudo fail2ban-client status apache
```

**Unban IP:**
```
sudo fail2ban-client set apache unbanip 111.111.111.111
```
