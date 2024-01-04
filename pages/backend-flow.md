# BACK-END FLOW
## Set up Express, knex, SQLite3 database and API
This file describes a process to create a back-end project using __Node__, __Express__, __knex__ and __SQLite3__. It sets up the server, database and API (endpoints & model files to perform CRUD operations on the database).

1. Make project folder & navigate into it

1. Create __package.json__
	```
	npm init -y
	```

1. Install dependencies (Express, knex, SQLite3, etc.)
	```
	npm install express knex sqlite3 nodemon
	```
	Include __nodemon__ for server reload on save, if desired.

1. If its not there, create __.gitignore__ file with the following line:
	```
	node_modules
	```
	During pushes to GitHub, this will stop all of the Node modules from being pushed up.

1. Create __index.js__ (see sample index.js & server.js, below). Make sure to:
	1. Import Express
	1. Set up an Express server
	1. Create async endpoint (can be in routers)

1. Edit __package.json__ scripts. Add a script to start the server.
	```
	"server": "nodemon index.js"
	```

1. Create __knexfile__ for JavaScript access to database:
	```
	knex init
	```
	If knex is not globally installed, run:
	```
	npx knex init
	```

1. Edit knexfile
	1. Keep development object. Remove staging & production objects.
	1. Specify database path & filename. For example:
		```javascript
		connection: {
		  filename: './data/recipeBook.db3'
		},
		```
	1. Add the following to prevent SQLite3 crashes:
		```javascript
		"useNullAsDefault: true",
		```
	1. Add path to migrations files. For example:
		```javascript
	    migrations: {
	      directory: './data/migrations'
	    }
		```

1. Create connection to database in index.js or elsewhere, like in a dedicated config file (maybe in /data). This will be imported into any files that need database access, like the router files (const db = require('../data/dbConfig')).
	```javascript
	const knex = require("knex")
	const knexfile = require("../knexfile")

	// selects development object from knexfile
	const db = knex(knexfile.development)

	module.exports = db
	```

1. Open TablePlus and create tables OR __create migrations__. When run, migration files will create and/or modify tables in the database specified in 8.2, above.
	1. Use the following command in the terminal:
		```
		knex migrate:make [migration-name]
		```
		For example:
	   	```
		knex migrate.make recipes
		```
	1. edit the UP and DOWN functions in migration file

1. Run migrations with:
	```
	knex migrate:latest
	```

1. For each resource in the project, create a __model file__ with find (all), findById, create, update, remove (or just what's needed for MVP). Once created, export them and __create routes__.
	1. Model files contain functions to perform interactions with the database. CRUD operations and the like are stored here. They allow these functions to be abstracted and reused by other components in an application.
	1. Routers then call the functions in the model files to communicate with the database.
___

### BASIC FILE CREATION ORDER:
During a Q&A, someone asked about the order that files were created when setting up a back-end with Express, knex & SQLite3. This was the answer we were given. The number indicates the step, above, in which the file is created.
* package.json (2)
* index.js (and optional server/router files) (5)
* knexfile.js (7)
* migrations (10)
___

### index.js example:
```javascript
const server = require('./server')

const PORT = process.env.PORT || 5000

server.listen(PORT, () => {
    console.log(`Server running on port ${PORT}`)
})
```
___

### server.js example:
```javascript
const express = require('express');
const server = express();
// const projectRouter = require('./routers/projectRouter');
// const resourceRouter = require('./routers/resourceRouter');
// const taskRouter = require('./routers/taskRouter');

server.use(express.json());
// server.use('/projects', projectRouter);
// server.use('/resources', resourceRouter);
// server.use('/tasks', taskRouter);

module.exports = server;
```
___

### projectsRouter.js example:
```javascript  
const express = require('express')
const router = express.Router()
const db = require('../data/dbConfig')

// GET all projects
router.get('/', async (req, res, next) => {
    try {
        const projects = await db.select("*").from("project")
        res.status(200).json(projects)
    } catch (error) {
        next(error)
    }
})

// POST new project
router.post('/', async (req, res, next) => {
    try {
        const newProjectID = await db

        .insert({
            name: req.body.name,
            description: req.body.description,
            completed: req.body.completed
        })
        .into("project")

        const viewProject = await db("project").where("id", newProjectID).limit(1)
        res.status(201).json(viewProject)
    } catch (error) {
        next(error)
    }
})

module.exports = router
```
___
### Look here for more router & model examples. Routers are in the '/routers' folder and models are in the '/data/models' folder:
* [Recipes back-end project](https://github.com/vishalicious213/14.4-node-db4-project)