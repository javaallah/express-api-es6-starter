# Express API ES6 Starter

Starter application for building APIs with [Express.js](http://expressjs.com/).

Comes with:

* [ES6](http://babeljs.io/learn-es2015/) features/modules
* ES7 [async](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/async_function)/[await](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/await)
* [Bookshelf](http://bookshelfjs.org/) ORM and [Knex](http://knexjs.org/) migrations
* PostgreSQL (default) with support for MySQL and SQLite
* API documentation using [swagger-ui](https://www.npmjs.com/package/swagger-ui) and [swagger-jsdoc](https://www.npmjs.com/package/swagger-jsdoc)
* [ESLint](http://eslint.org/) for code linting
* Request validation using [Joi](https://www.npmjs.com/package/joi)
* Logging using [winston](https://www.npmjs.com/package/winston)
* Application configuration using [dotenv](https://www.npmjs.com/package/dotenv)
* Tests using [mocha](https://www.npmjs.com/package/mocha), [supertest](https://www.npmjs.com/package/supertest) and [chai](https://www.npmjs.com/package/chai)

---

## Installation

Clone the repository, install the dependencies and get started right away.

    $ git clone git@github.com:mesaugat/express-api-es6-starter.git <application-name>
    $ cd <application-name>
    $ rm -rf .git
    $ npm install

Make a copy of `.env.example` as `.env` and update your application details and database credentials. Now, run the migrations and seed the database.

    $ npm run migrate:latest
    $ npm run seed

Finally, start the application:

    $ npm run start:dev (For development)
    $ npm start (For production)

Navigate to `/api-docs` for the API documentation.

## Tests

To run the tests you need to create a separate test database. Don't forget to update your `.env` file to include the name of the test database and run the migrations.

    $ NODE_ENV=test npm run migrate:latest
    $ npm test

## Using MySQL instead of PostgreSQL

Install [mysql](https://www.npmjs.com/package/mysql) driver and update this line `DB_CLIENT='pg'` in your .env file to `DB_CLIENT='mysql'`. You can remove the [pg](https://www.npmjs.com/package/pg) driver if you like to.

    $ npm install mysql --save
    $ npm uninstall pg --save

## Contributing

For contribution and feature requests, please create an [issue](https://github.com/mesaugat/express-api-es6-starter/issues) first.

## License

express-api-es6-starter is under [MIT License](http://www.opensource.org/licenses/MIT).
