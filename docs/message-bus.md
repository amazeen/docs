# Message Bus

## Messages

### Request Admin users list
```
{
    type: 'admin:request-list'
}
```

### Admin users list Response
```
{
    type: 'admin:list'
    data: [
        {
            username: String
            email: String
            phone: String
        }
    ]
}
```


### Admin user updated
```
{
    type: 'admin:updated'
    data: {
        username: String
        email: String
        phone: String
    }
    
}
```

### New Reading Received
```
{
    type: 'parameter:reading'
    data: {
        area: Integer
        silo: Integer
        type: String
        value: Double
        active: Boolean (if type == capacity)
    }
    
}
```

### Threshold Reached
```
{
    type: 'parameter:threshold-reached'
    data: {
        area: Integer
        silo: Integer
        type: String
        value: Double
    }
    
}
```
