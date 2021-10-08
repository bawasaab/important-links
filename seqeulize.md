
npm install --save sequelize
npm install --save-dev sequelize-cli
npx sequelize-cli init

goto the config folder for db configs

# One of the following:
$ npm install --save pg pg-hstore # Postgres
$ npm install --save mysql2
$ npm install --save mariadb
$ npm install --save sqlite3
$ npm install --save tedious # Microsoft SQL Server

GENERATE MODEL
npx sequelize-cli model:generate --name User --attributes firstName:string,lastName:string,email:string

Running Migrations
npx sequelize-cli db:migrate

Undoing Migrations
npx sequelize-cli db:migrate:undo
db:migrate:undo:all

You can also revert back to a specific migration by passing its name in --to option.
npx sequelize-cli db:migrate:undo:all --to XXXXXXXXXXXXXX-create-posts.js

You can also revert back to a specific migration by passing its name in --to option.

npx sequelize-cli db:migrate:undo:all --to XXXXXXXXXXXXXX-create-posts.js

Creating the first Seed
npx sequelize-cli seed:generate --name demo-user

RUN SEED
npx sequelize-cli db:seed:all

UNDO SEEDS
If you wish to undo the most recent seed:

npx sequelize-cli db:seed:undo
If you wish to undo a specific seed:

npx sequelize-cli db:seed:undo --seed name-of-seed-as-in-data
If you wish to undo all seeds:

npx sequelize-cli db:seed:undo:all




sequelize db:migrate                        Run pending migrations
sequelize db:migrate:schema:timestamps:add  Update migration table to have timestamps
sequelize db:migrate:status                 List the status of all migrations
sequelize db:migrate:undo                   Reverts a migration
sequelize db:migrate:undo:all               Revert all migrations ran
sequelize db:seed                           Run specified seeder
sequelize db:seed:undo                      Deletes data from the database
sequelize db:seed:all                       Run every seeder
sequelize db:seed:undo:all                  Deletes data from the database
sequelize db:create                         Create database specified by configuration
sequelize db:drop                           Drop database specified by configuration
sequelize init                              Initializes project
sequelize init:config                       Initializes configuration
sequelize init:migrations                   Initializes migrations
sequelize init:models                       Initializes models
sequelize init:seeders                      Initializes seeders
sequelize migration:generate                Generates a new migration file      [aliases: migration:create]
sequelize model:generate                    Generates a model and its migration [aliases: model:create]
sequelize seed:generate                     Generates a new seed file 






==============================================================================================================================================================================
EXAMPLE MIGRATION STARTS
==============================================================================================================================================================================

'use strict';
var dated = new Date();
module.exports = {
  up: async (queryInterface, Sequelize) => {
    await queryInterface.createTable('Users', {
      id: {
        allowNull: false,
        autoIncrement: true,
        primaryKey: true,
        type: Sequelize.INTEGER
      },
      first_name: {
        type: Sequelize.STRING,
        allowNull: false
      },
      last_name: {
        type: Sequelize.STRING
      },
      email: {
        type: Sequelize.STRING,
        allowNull: false,
        unique: true
      },
      password: {
        type: Sequelize.STRING,
        allowNull: false
      },
      dob: {
        type: Sequelize.DATE
      },
      role: {
        type: Sequelize.ENUM('ADMIN','USER'),
        allowNull: false
      },
      status: {
        type: Sequelize.ENUM('OPEN', 'CLOSE', 'DELETED'),
        allowNull: false
      },
      deletedAt: {
        allowNull: true,
        type: Sequelize.DATE
      },
      createdAt: {
        allowNull: false,
        type: Sequelize.DATE,
        defaultValue: dated
      },
      updatedAt: {
        allowNull: true,
        type: Sequelize.DATE
      }
    });
  },
  down: async (queryInterface, Sequelize) => {
    await queryInterface.dropTable('Users');
  }
};
==============================================================================================================================================================================
EXAMPLE MIGRATION ENDS
==============================================================================================================================================================================


==============================================================================================================================================================================
EXAMPLE MODEL STARTS
==============================================================================================================================================================================

'use strict';
const {
  Model
} = require('sequelize');
module.exports = (sequelize, DataTypes) => {
  class User extends Model {
    /**
     * Helper method for defining associations.
     * This method is not a part of Sequelize lifecycle.
     * The `models/index` file will call this method automatically.
     */
    static associate(models) {
      // define association here
    }
  };
  User.init({
    first_name: DataTypes.STRING,
    last_name: DataTypes.STRING,
    email: DataTypes.STRING,
    password: DataTypes.STRING,
    dob: DataTypes.DATE,
    role: DataTypes.ENUM('ADMIN', 'USER'),
    status: DataTypes.ENUM('OPEN', 'CLOSE', 'DELETED'),
    deletedAt: DataTypes.DATE,
  }, {
    sequelize,
    modelName: 'User',
  });
  return User;
};

==============================================================================================================================================================================
EXAMPLE MODEL ENDS
==============================================================================================================================================================================


==============================================================================================================================================================================
EXAMPLE SEEDER STARTS
==============================================================================================================================================================================

'use strict';
var dated = new Date();
module.exports = {
  up: async (queryInterface, Sequelize) => {
    /**
     * Add seed commands here.
     *
     * Example:
     * await queryInterface.bulkInsert('People', [{
     *   name: 'John Doe',
     *   isBetaMember: false
     * }], {});
    */

     await queryInterface.bulkInsert('Users', [{
        first_name: 'Deepak',
        last_name: 'Bawa',
        email: 'bawa_d@ymail.com',
        password: '123456',
        dob: dated,
        role: 'USER',
        status: 'OPEN',
        createdAt: dated
      }], {});
  },

  down: async (queryInterface, Sequelize) => {
    /**
     * Add commands to revert seed here.
     *
     * Example:
     * await queryInterface.bulkDelete('People', null, {});
     */
     await queryInterface.bulkDelete('Users', null, {});
  }
};


==============================================================================================================================================================================
EXAMPLE SEEDER ENDS
==============================================================================================================================================================================


==============================================================================================================================================================================
EXAMPLE CRUD STARTS
==============================================================================================================================================================================

var User = require('../models').User;
const Op = require('sequelize').Op;

module.exports = class UsersController {

    constructor() {
        console.log('inside controller constructor');
    }

    getAllUsers( req, res, next ) {
        try {
            User.findAll(
            {
                attributes: ['first_name', 'last_name', 'email', 'dob', 'status'],
                where: {
                    status: {
                        [Op.ne]: 'DELETED' 
                    } 
                }
            }
            ).then((result) => {
        
                if (result === null) {
    
                    return res.send({
                        status: 200,
                        code: 404,
                        msg: 'Records not found',
                        data: result
                    });
                } else {
    
                    return res.send({
                        status: 200,
                        code: 200,
                        msg: 'Records found',
                        data: result
                    });
                }
            })
            .catch((error) => {
    
                res.send({
                    status: 400,
                    code: 400,
                    msg: 'Exception occur',
                    data: error.toString()
                });
            });
        } catch(ex) {
            console.log('catch');
    
            return res.send({
                status: 400,
                code: 400,
                msg: 'Exception occur',
                data: ex.toString()
            });
        }
    }

    getUserById( req, res, next ) {
        try {
            let id = req.params.id;
            User.findOne(
                { 
                    where: { 
                        id: id,
                        status: { 
                            [Op.ne]: 'DELETED' 
                        } 
                    } 
                }
            )
            .then((result) => {

                if (result === null) {
    
                    return res.send({
                        status: 200,
                        code: 404,
                        msg: 'Records not found',
                        data: result
                    });
                } else {
    
                    return res.send({
                        status: 200,
                        code: 200,
                        msg: 'Records found',
                        data: result
                    });
                }
            })
            .catch((error) => {

                res.send({
                    status: 400,
                    code: 400,
                    msg: 'Exception occur',
                    data: error.toString()
                });
            });
        } catch(ex) {
            console.log('catch');
    
            return res.send({
                status: 400,
                code: 400,
                msg: 'Exception occur',
                data: ex.toString()
            });
        }
    }  
    
    insertUser( req, res, next ) {
        try {
            let in_data = req.body;

            User.build(in_data).save()
            .then((result) => {

                if (result === null) {
    
                    return res.send({
                        status: 200,
                        code: 404,
                        msg: 'Record not inserted',
                        data: result
                    });
                } else {
    
                    return res.send({
                        status: 200,
                        code: 200,
                        msg: 'Record inserted successfully',
                        data: result
                    });
                }
            })
            .catch((error) => {

                res.send({
                    status: 400,
                    code: 400,
                    msg: 'Exception occur',
                    data: error.toString()
                });
            });
        } catch(ex) {
            console.log('catch');
    
            return res.send({
                status: 400,
                code: 400,
                msg: 'Exception occur',
                data: ex.toString()
            });
        }
    }

    updateUser( req, res, next ) {
        try {
            let id = req.params.id;
            let in_data = req.body;

            User.update(in_data, { where: { id: id } })
            .then((result) => {

                if (result === null) {
    
                    return res.send({
                        status: 200,
                        code: 404,
                        msg: 'Record not updated',
                        data: result
                    });
                } else {
    
                    return res.send({
                        status: 200,
                        code: 200,
                        msg: 'Record updated successfully',
                        data: result
                    });
                }
            })
            .catch((error) => {

                res.send({
                    status: 400,
                    code: 400,
                    msg: 'Exception occur',
                    data: error.toString()
                });
            });

        } catch(ex) {
            console.log('catch');
    
            return res.send({
                status: 400,
                code: 400,
                msg: 'Exception occur',
                data: ex.toString()
            });
        }
    }

    deleteUser( req, res, next ) {
        try {
            let id = req.params.id;
            let dated = new Date();
            let in_data = {
                status : 'DELETED',
                deletedAt: dated
            };

            User.update(in_data, { where: { id: id } })
            .then((result) => {

                if (result === null) {
    
                    return res.send({
                        status: 200,
                        code: 404,
                        msg: 'Record not updated',
                        data: result
                    });
                } else {
    
                    return res.send({
                        status: 200,
                        code: 200,
                        msg: 'Record updated successfully',
                        data: result
                    });
                }
            })
            .catch((error) => {

                res.send({
                    status: 400,
                    code: 400,
                    msg: 'Exception occur',
                    data: error.toString()
                });
            });

        } catch(ex) {
            console.log('catch');
    
            return res.send({
                status: 400,
                code: 400,
                msg: 'Exception occur',
                data: ex.toString()
            });
        }
    }

    deleteHardUser( req, res, next ) {
        try {
            let id = req.params.id;
            User.destroy({ where: { id: id } })
            .then((result) => {

                if (result === null) {
    
                    return res.send({
                        status: 200,
                        code: 404,
                        msg: 'Record not deleted',
                        data: result
                    });
                } else {
    
                    return res.send({
                        status: 200,
                        code: 200,
                        msg: 'Record deleted successfully',
                        data: result
                    });
                }
            })
            .catch((error) => {

                res.send({
                    status: 400,
                    code: 400,
                    msg: 'Exception occur',
                    data: error.toString()
                });
            });

        } catch(ex) {
            console.log('catch');
    
            return res.send({
                status: 400,
                code: 400,
                msg: 'Exception occur',
                data: ex.toString()
            });
        }
    }
}

==============================================================================================================================================================================
EXAMPLE CRUD ENDS
==============================================================================================================================================================================

https://zetcode.com/javascript/sequelize/

let result = await Instruments.findAll({
                attributes: ['id', 'instrument_token', 'exchange_token', 'tradingsymbol', 'name', '	last_price', 'expiry', 'strike', 'tick_size', 'lot_size', 'instrument_type', 'segment', 'exchange', 'createdAt', 'updatedAt', '	deletedAt'],
                offset: 0, 
                limit: 10,
                order: [['id', 'DESC']],
                raw: true 
            });
