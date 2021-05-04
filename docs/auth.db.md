# Auth DB

PostgreSQL has been chosen as db

## Structure

### Users
```
username: String primary key
hash: Hash not null
roles: String foreign key
email: string
```

### Roles
```
name: String primary key
permissions: array[String] not null 
```