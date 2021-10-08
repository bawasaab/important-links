MYSQL

This is as a result of some files in C:\xampp\mysql\data\mysql getting corrupted.

Solution:

Back up C:\xampp\mysql\data
Copy all file C:\xampp\mysql\backup
Paste and replace existing file in: C:\xampp\mysql\data, except for the ibdata1 file.
Leaving ibdata1 will help against table does not exist error.


Apache - MySQL Service detected with wrong path. / Ports already in use
https://stackoverflow.com/questions/15718157/apache-mysql-service-detected-with-wrong-path-ports-already-in-use
1. Go to cmd and run it with Administrator mode.
2. Uninstall mysql service through command prompt using the following command.

        sc delete mysql
3. restart XAMPP
