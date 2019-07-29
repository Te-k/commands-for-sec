# journalctl

**Check for a specific unit:**
```
journalctl -u nginx.service
```

**Limit in time:**
```
journalctl --since 09:00 --until "1 hour ago"
journalctl -u nginx.service --since today
```
