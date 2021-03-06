![image_squidhome@2x.png](http://i.imgur.com/RIvu9.png) 

# MySQLAdapter

Adds MySQL support for Sails.

# Sails.js Repo
http://SailsJs.org

## Installation

Install from NPM.

```bash
$ npm install sails-mysql
```

## Sails Configuration

Add the mysql config to the config/adapters.js file.  Basic options:

```javascript
module.exports.adapters = {
  'default': 'mysql',

  mysql: {
    module   : 'sails-mysql',
    host     : 'localhost',
    port     : 3306,
    user     : 'username',
    password : 'password',
    database : 'MySQL Database Name'
    
    // OR (exlicit sets take precedence)
    module   : 'sails-mysql',
    url      : 'mysql2://USER:PASSWORD@HOST:PORT/DATABASENAME'
    }
  }
};
```

## Run tests

You can set environment variables to override the default database config for the tests, e.g.:

```sh
$ WATERLINE_ADAPTER_TESTS_PASSWORD=yourpass npm test
```


Default settings are:

```javascript
{
  host: process.env.WATERLINE_ADAPTER_TESTS_HOST || 'localhost',
  user: process.env.WATERLINE_ADAPTER_TESTS_USER || 'root',
  password: process.env.WATERLINE_ADAPTER_TESTS_PASSWORD || '',
  database: process.env.WATERLINE_ADAPTER_TESTS_DATABASE || 'sails_mysql',
  pool: true,
  connectionLimit: 10,
  waitForConnections: true
}
```


## About Waterline
Waterline is a new kind of storage and retrieval engine.  It provides a uniform API for accessing stuff from different kinds of databases, protocols, and 3rd party APIs.  That means you write the same code to get users, whether they live in mySQL, LDAP, MongoDB, or Facebook.
Waterline also comes with built-in transaction support, as well as a configurable environment setting. 

 

[![githalytics.com alpha](https://cruel-carlota.pagodabox.com/a22d3919de208c90c898986619efaa85 "githalytics.com")](http://githalytics.com/mikermcneil/sails-mysql)
