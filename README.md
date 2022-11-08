# Example Readme
When publishing a code repository for any app, it's a good idea to create a README.md at the root that will instruct the reader/viewer how to run the app.  Let this be an example.

---
START EXAMPLE
---
# My Amazing Web App
A cool web app that does stuff

## Getting Started

    npm i
    createdb some-name

Run `npm run server:dev` to start the web server.
In a second terminal navigate back to the local repo and run `npm run client:dev` to start the react server. 
Run `db:build` which rebuilds the database, all the tables, and ensures that there is meaningful data present.

## Deployed URL
[example.com - hosted on heroku](example.com)
    
## Environment Variables

    DB_URL=<your-database-connection-string>
    JWT_SECRET=some-very-secret-key
    SOME_ENV_VAR=something-else-cool

## Tech Stack
### Backend: Node.js, Express.js, PostgreSQL
It all starts in the root `index.js` file.  This is the express server.  The routing middleware is handled in this file as well.

### Frontend: React.js, Stripe, Material-UI
The root React code starts in the `src/index.js` file.

## Project Structure

```bash
├── db
│   ├── index.js
│   └── init_db.js
├── index.js
├── package.json
├── public
│   └── index.html
├── routes
│   └── index.js
└── src
    ├── api
    │   └── index.js
    ├── components
    │   ├── App.js
    │   └── index.js
    └── index.js
```

Top level `index.js` is our Express Server. This is responsible for setting up our API, starting our server, and connecting to our database.

Inside `/db` we have `index.js` which is responsible for creating all of our database connection functions.

Inside `/routes` we have `index.js` which is responsible for building the `apiRouter`, which is attached in the express server. This will build all routes that our React application will use to send/receive data via JSON.

Lastly `/public` and `/src` are the two puzzle pieces for our React front-end. `/public` contains any static files necessary for our front-end, and `/src` is our React source code.
