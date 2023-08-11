# E-Commerce Backend - Module 13

The E-Commerce Backend is a SQL (Sequelize) backend database containing products, tags, and categories 


## Prerequisites

Before you begin, ensure you have installed:

- [Node.js](https://nodejs.org/)
- [npm](https://www.npmjs.com/get-npm) (comes with Node.js)
- A MySQL server (Local or hosted)

## Dependencies

This project uses the following Node.js packages:

- `express` for interacting with the database routes.
- `sequelize` to connect to a MySQL database.

You can install these by running `npm install` in the root directory of the project.

## Usage

1. First, you need to set up your database connection. Update the `connection.js` file in the root directory of the project with the following content, replacing `'ecommerce_db'`, `'user'`, and `'somepass'` with your actual MySQL connection details:

```javascript
require('dotenv').config();

const Sequelize = require('sequelize');

const sequelize = process.env.JAWSDB_URL
  ? new Sequelize(process.env.JAWSDB_URL)
  : new Sequelize("ecommerce_db", "user", "somepass", {
      host: 'localhost',
      dialect: 'mysql',
      dialectOptions: {
        decimalNumbers: true,
      },
    });

module.exports = sequelize;

...
```

2. To start the application, open a terminal in the root directory of the project and run:

```bash
node server.js
```

3. To create the database use the schema provided in db/schema.sql

4. To seed the database run the seed file in seeds/index.js
```bash
node index.js
```
... 

## Live Video
URL: [https://www.loom.com/share/eb15262322ac4c8196069caf0c4aa313](https://www.loom.com/share/a303819e911744da94429a763f705de8)


## Contributing

Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.

## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details.
