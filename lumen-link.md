https://auth0.com/blog/developing-restful-apis-with-lumen/

https://medium.com/tech-tajawal/jwt-authentication-for-lumen-5-6-2376fd38d454

https://github.com/barryvdh/laravel-cors
https://stackoverflow.com/questions/34476817/lumen-enable-cors
https://gist.github.com/danharper/06d2386f0b826b669552
https://stackoverflow.com/questions/46996130/lumen-api-cors-ajax-405-method-not-allowed
https://thewebtier.com/laravel/handle-cors-requests-vuejs-client-laravel-api/
https://stackoverflow.com/questions/49124228/showing-mysql-error-for-db-class-in-laravel
https://stackoverflow.com/questions/44815838/laravel-lumen-mail-and-amazon-ses-500-internal-server-error-on-ubuntu-server-pr

// creating index
ALTER TABLE `straw`.`user_notification_settings` ADD INDEX `userId` (`id`);

// CORS ISSUE
https://stackoverflow.com/questions/46996130/lumen-api-cors-ajax-405-method-not-allowed/47012740#47012740

php artisan route:list

// THIS IS MORE FEASIBLE
php artisan make:model Todo -a

php artisan make:migration create_users_table
php artisan migrate:refresh

// Refresh the database and run all database seeds...
php artisan migrate:refresh --seed

// Drop All Tables & Migrate
php artisan migrate:fresh

php artisan migrate:fresh --seed

https://www.larashout.com/using-soft-delete-in-laravel-eloquent-models

php artisan make:migration create_rel_user_countries_table

composer dump-autoload -o
php artisan migrate
php artisan db:seed

https://arjunphp.com/laravel-create-controller-model-migration-one-artisan-command/
Artisan is the command-line interface included with Laravel. It provides a number of helpful commands that can assist you while you build your application. Here I am gonna show you a command which will generate controller, modal and migration files.

php artisan make:model Modelname -crm
php artisan make:model Modelname -crm
As you can see, actually the command is for creating modal but by passing -crm arguments we can generate controller and migration files.

Console output might be as shown below –

$ php artisan make:model Modelname -crm
Model created successfully.
Created Migration: 2017_06_03_150652_create_modelnames_table
Controller created successfully.
$ php artisan make:model Modelname -crm
Model created successfully.
Created Migration: 2017_06_03_150652_create_modelnames_table
Controller created successfully.

countryId


https://pusher.com/tutorials/web-notifications-laravel-pusher-channels
https://quickadminpanel.com/blog/list-of-16-artisan-make-commands-with-parameters/
https://github.com/davibennun/laravel-push-notification

https://stackoverflow.com/questions/39335363/fcm-notification-in-ios-doesnt-play-sound-when-received

update `polls` set published_at = '2019-05-22 08:27:08', created_at = '2019-05-22 08:27:08', updated_at = '2019-05-22 08:27:08'


// log query in lumen
$queries    = DB::getQueryLog();
$lastQuery = end($queries);

Log::info($lastQuery);



// READ LOGS
tail -f laravel.log


https://stackoverflow.com/questions/60268308/laravel-6-throttle-password-reset





In my opinion how you are approaching it is fine:

response is the full response object via axios
response.data is the full response body that was returned
response.data.data is the data node of the response body that was returned
Some suggestions:

instead of using success in your response, that can be implied from the returned status code: anything within 200-299 is successful, anything 300-399 is a redirect, anything 400-499 is a client error, and anything 500+ is a server error (see here)
instead of using data in the instance of an error, in my opinion that node should be reserved for successful data and a node such as errors should be used instead
your sendError method should default to a status code of 500 instead of 200, as 200 is a successful status code
