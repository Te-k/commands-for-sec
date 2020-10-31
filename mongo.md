# mongo

**Connect to remote DB:**
```
mongo -u <USER> -p <PASSWORD> <HOST:PORT/DB>
```

**List databases:**
```
show dbs
```

**List collections**:
```
show collections
```

**Show content of the collection cars**:
```
db.cars.find()
```

**Drop the collection houses**
```
db.houses.drop()
```

**Dump database:**
```
mongodump -d <database_name> -o <directory_backup>
```

**Restore dump:**
```
mongorestore -d <database_name> <directory_backup>
```
