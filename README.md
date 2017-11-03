Framework for RESTful API's on node

![The Parkes Radio Telescope](https://upload.wikimedia.org/wikipedia/commons/thumb/2/22/ParkesTelescopeNight.png/800px-ParkesTelescopeNight.png)
https://upload.wikimedia.org/wikipedia/commons/thumb/2/22/ParkesTelescopeNight.png/800px-ParkesTelescopeNight.png

## Features

* Just define your database models and you have a simple API
* Keeps internal DB ids hidden, using a UUID or similar for public IDs ([see why](http://toddfredrich.com/ids-in-rest-api.html))
* Automatically handles includes and joins for associations
* Simple definition of public and private attributes
* Uniform JSON errors
* **Get a working API up in 5 minutes**

Parkes is built upon [koa2](https://github.com/koajs/koa) and [sequelize](https://docs.sequelizejs.com) and requires at least node 7.6

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

# License

© 2017 Agency Ventures
