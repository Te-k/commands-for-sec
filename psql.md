# PostGresQL

**Connect to psql with postgres user (most common local authent)**
```bash
sudo -u postgres psql
```

**Connect with psql**
```bash
psql -h <host> -p <port> -u <database>
psql -h <host> -p <port> -U <username> -W <password> <database>
```

**List tables**
```
\dt
```

**List databases**
```
\l
```

**List users:**
```
\du
```

**Use a database:**
```
\c DATABASE
```
