# More Queries


![image](https://user-images.githubusercontent.com/105078661/219197011-52f7460e-0f2a-4e0a-a094-f3f6f84f3ae9.png)

## Use “container-on-demand” to run MySQL:

- In the container, credentials are root/root

  - Ask for container Ubuntu 20.04
  - Connect via SSH
  - OR connect via the Web terminal
  - In the container, you should start MySQL before playing with it:
  
 $ service mysql start                                                   
 * Starting MySQL database server mysqld 
$
$ cat 0-list_databases.sql | mysql -uroot -p                               
Database                                                                                   
information_schema                                                                         
mysql                                                                                      
performance_schema                                                                         
sys                      
$

## How to import a SQL dump:

$ echo "CREATE DATABASE hbtn_0d_tvshows;" | mysql -uroot -p
Enter password: 
$ curl "https://s3.amazonaws.com/intranet-projects-files/holbertonschool-higher-level_programming+/274/hbtn_0d_tvshows.sql" -s | mysql -uroot -p hbtn_0d_tvshows
Enter password: 
$ echo "SELECT * FROM tv_genres" | mysql -uroot -p hbtn_0d_tvshows
Enter password: 
id  name
1   Drama
2   Mystery
3   Adventure
4   Fantasy
5   Comedy
6   Crime
7   Suspense
8   Thriller
$

![image](https://user-images.githubusercontent.com/105078661/219200048-b92e1876-db35-4334-9302-b9cadcc8dbe2.png)
