Framework for RESTful API's on node

Features
* Just define your database models and you have a simple API
* Keeps internal DB ids hidden, using a UUID or similar for public IDs ([see why](http://toddfredrich.com/ids-in-rest-api.html))
* Automatically handles includes and joins for associations
* Simple definition of public and private attributes
* Uniform JSON errors
* Get a skeleton API up in 5 minutes

Parkes is built upon koa2 and sequelize and requires node 7.6

```bash
npm install -G parkes

# Initialize a new api
parkes init my-api

cd my-api

parkes generate scaffold post
parkes generate scaffold user

# Gives you
# User and Post models
api/models/post.js
api/models/user.js

migrations/create-post.js
migrations/create-user.js

# Database configuration
api/config/database.js

# User and Post controllers
api/v1/controllers/post.js
api/v1/controllers/user.js

# Node server stack
server.js
```
