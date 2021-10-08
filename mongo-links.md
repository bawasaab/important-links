#MONGO INSTALLATION

https://docs.mongodb.com/manual/tutorial/install-mongodb-on-ubuntu/

1. Import the public key used by the package management system
    wget -qO - https://www.mongodb.org/static/pgp/server-4.2.asc | sudo apt-key add -
    
2. However, if you receive an error indicating that gnupg is not installed, you can
    sudo apt-get install gnupg
    
3. repeat step 1

4. echo "deb [ arch=amd64,arm64 ] https://repo.mongodb.org/apt/ubuntu bionic/mongodb-org/4.2 multiverse" | sudo tee /etc/apt/sources.list.d/mongodb-org-4.2.list

5. sudo apt-get update

6. sudo apt-get install -y mongodb-org

7. Optional. Although you can specify any available version of MongoDB, apt-get will upgrade the packages when a newer version becomes available. To prevent unintended upgrades, you can pin the package at the currently installed version:
    echo "mongodb-org hold" | sudo dpkg --set-selections
    echo "mongodb-org-server hold" | sudo dpkg --set-selections
    echo "mongodb-org-shell hold" | sudo dpkg --set-selections
    echo "mongodb-org-mongos hold" | sudo dpkg --set-selections
    echo "mongodb-org-tools hold" | sudo dpkg --set-selections

8. Start MongoDB
    sudo systemctl start mongod
    
9. if Failed to start mongod.service: Unit mongod.service not found.
    sudo systemctl daemon-reload

10. Verify that MongoDB has started successfully
    sudo systemctl status mongod
    
11. You can optionally ensure that MongoDB will start following a system reboot by issuing the following command:
    sudo systemctl enable mongod
    
12. Stop MongoDB
    sudo systemctl stop mongod
 
13. restart mongoDB
    sudo systemctl restart mongod
    
14. Begin using MongoDB
   mongo
   
   UNINSTALL MONGO DB
15. Stop MongoDB service
  sudo service mongod stop
  
16. Remove Packages
  sudo apt-get purge mongodb-org*
  
17. Remove Data Directories
    sudo rm -r /var/log/mongodb
    sudo rm -r /var/lib/mongodb


http://ksat.me/

http://devblog.me/wtf-mongo

https://www.infoq.com/articles/Starting-With-MongoDB/


https://www.mongodb.com/blog/post/6-rules-of-thumb-for-mongodb-schema-design-part-1

https://blog.cloudboost.io/everything-you-need-to-know-about-mongoose-63fcf8564d52

https://ma.ttias.be/mariadb-json-datatype-supported-10-2/

https://scotch.io/tutorials/working-with-json-in-mysql

https://chartio.com/resources/tutorials/understanding-strorage-sizes-for-mysql-text-data-types/

https://www.cumulations.com/blogs/87/how-to-send-push-notifications-in-php-to-ios-devices-using-fcm

https://www.monitis.com/blog/101-tips-to-mysql-tuning-and-optimization/

https://stackoverflow.com/questions/39632667/how-to-kill-the-process-currently-using-a-port-on-localhost-in-windows

https://gist.github.com/prime31/5675017

https://gist.github.com/joashp/b2f6c7e24127f2798eb2

https://scotch.io/tutorials/mean-app-with-angular-2-and-the-angular-cli

http://jasonwatmore.com/post/2018/11/07/angular-7-reactive-forms-validation-example

https://stackoverflow.com/questions/22739455/htaccess-redirect-for-angular-routes


// angular htaccess
RewriteEngine on
RewriteCond %{REQUEST_FILENAME} -s [OR]
RewriteCond %{REQUEST_FILENAME} -l [OR]
RewriteCond %{REQUEST_FILENAME} -d
RewriteRule ^.*$ - [NC,L]

RewriteRule ^(.*) /index.html [NC,L]


mongodb://<username>:<password>@main-shard-00-00-03xkr.mongodb.net:27017,main-shard-00-01-03xkr.mongodb.net:27017,main-shard-00-02-03xkr.mongodb.net:27017/main?ssl=true&replicaSet=Main-shard-0&authSource=admin&retryWrites=true


{
   $lookup:
     {
       from: <collection to join>,
       localField: <field from the input documents>,
       foreignField: <field from the documents of the "from" collection>,
       as: <output array field>
     }
}
