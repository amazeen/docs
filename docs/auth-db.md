# Auth DB

MongoDB has been chosen as db

## Structure

### Users
```
{
  "_id": {"$oid": Auto id},
  "username": String,
  "password": Hash,
  "role": String nullable,
  "email": String nullable,
  "phone": Integer nullable
}
email: string
```

### Roles
```
{
  "_id":{"$oid": Auto id},
  "persissions":[String],
  "role": String
}
```
