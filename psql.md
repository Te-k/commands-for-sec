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

**Dump from docker :**
```
docker exec -t your-db-container pg_dumpall -c -U postgres > dump_`date +%d-%m-%Y"_"%H_%M_%S`.sql
```
