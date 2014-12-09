coal
----------------
  ORM Base on [knexjs](http://knexjs.org)


## Install

```shell
npm install coal --save
```

## Getting start


### database configure

configure.coffee

```coffeescript
module.exports =
  database:
    client: 'mysql'
    connection:
      host: 'localhost'
      user: 'root'
      password: '123456'
      database: 'test_coal'
  schema: 'schame'
```

init tables

```coffeescript
Coal = require 'coal'
config = require './config'
coal = new Coal(config)
```

## API

### coal.Model(tableName)

return an instance of Model.

### Model.save(obj)

return promises

### Model.update(obj[, where])

```where``` argument is optional. it must be array, like ["id", "=", 1]

return promises

### Model.find(fields[, where])

param ```fields``` must be array. 

return promises

### Model.findOne(fields[, where])

the same with up.

### Model.delOne(key, value)

return promises

### Model.delMul(key, valueArray)

return promises

### Model.sql(sql)

param ```sql``` is a sql string. like ```select * from people```

return promises

### Model.tab()

return a knex instance.

## Sample

see the directory ```sample```

## LICENSE

MIT

## History

v0.0.2

  support simple operate function. like: save, update, delOne, delMul, sql and so on

v0.0.1

  init coal