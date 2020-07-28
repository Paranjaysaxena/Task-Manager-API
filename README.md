# Task-Manager-API

## A simple REST API with authentication which can create users and create tasks.  Features include:

- Pagination and filtering of server responses to avoid slow page load times.
- Full CRUD features for User and Task instances.
- Hash encryption of passwords and access management with JWT tokens.  
- Restricted user access to CRUD operations based on JWT tokens.
- This API was built for training purpose.

### SETUP INSTRUCTIONS

To use this code you will require an account with [SendGrid](https://signup.sendgrid.com/).  Sign-up is free and no credit card is required to access a free-tier API Key.

Node.js version 12+ and npm must be installed on your machine.  In terminal type the following commands:
```
git clone https://github.com/Paranjaysaxena/Task-Manager-API.git
cd task-manger-api
sudo npm install
mkdir config
cd config
touch dev.env
vim dev.env
```

Insert the following lines in `dev.env`, replacing all `<content>` with your own information:

```
PORT=<port number>
SGMAIL_EMAIL=<your email address>
MONGODB_URL=<mongodb connection string>
SENDGRID_API_KEY=<api key>
JWT_SECRET=<unique key of your choice to generate JSON web tokens>
```

To run the web server return to the root of the repository and type:
```
npm run dev
```
Alternatively you may name `config/prod.env` or `config/staging.env` and appropriately run the web server with `npm run prod` or `npm run staging`.

## Server

The server is made on `nodejs` (v12.4.0)

`Express.js` is used as the server framework

## NPM Library

* `bcryptjs` - to encrypt plain password.

* `jsonwebtoken` - to create authentication token.

* `mongoose` - MongoDB library for JS.

* `multer` - to upload files.

* `sharp` - to convert large images in common formats to smaller, web-friendly JPEG, PNG and WebP images of varying dimensions.

* `validator` - to validate and sanitize string.


## API

* The base path of the API is `https://task-manager-todo-api.herokuapp.com/`

* The various requests and endpoints are:-

  * POST `/users` - to create user.

  * POST `/users/login` - to login.

  * POST `/users/logout` - to logout.

  * POST `/tasks` - to create tasks.

  * POST `/users/logoutAll` - to logout from all sessions.

  * GET `/users/me` - to get user profile.

  * GET `/tasks` - to get user tasks.

  * PATCH `/users/me` - to update user information.

  * PATCH `/tasks/<id of the task to be updates>` - to update task.

  * DELETE `users/me` - to delete user.

  * DELETE `/tasks/<id of the task to be updates>` - to delete task.

* Use POSTMAN to fire off the requests to the endpoints.

---
