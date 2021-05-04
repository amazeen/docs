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
    type: 'admin:response-list'
    data: [
        {
            username: String
            email: String
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
    }
    
}
```

### New Reading Received
```
{
    type: 'reading:new'
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
    type: 'reading:threshold-reached'
    data: {
        area: Integer
        silo: Integer
        type: String
        value: Double
    }
    
}
```

### Sensor Offline (Optional)
```
{
    type: 'sensor:offline'
    data: {
        area: Integer
        silo: Integer
        type: String
        identifier: String
    }
}
```
