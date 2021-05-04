# Data DB

InfluxDB/PostgreSQL have been chosen as db

InfluxDB will contain the raw readings
Postgres will contain the silo -> area mappings and the parameter thresholds

## InfluxDB

```
area: id
silo: id
type: string
value: double
active: boolean (if type == capacity)
```

## PostgreSQL

### Areas

```
id: primary key
```

### Silos

```
id: primary key
area_id: foreign key not null
```

### Thresholds

```
id: primary key
maximum: double
minimum: double
parameter_type: foreign key
silo_id: foreign key not null
```

### Parameter Types

```
type: string primary key
```