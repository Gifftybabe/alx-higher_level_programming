# More Queries


![image](https://user-images.githubusercontent.com/105078661/219212034-ed56294c-45e5-4c0d-b530-e38ce0bc58a1.png)

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

![image](https://user-images.githubusercontent.com/105078661/219213698-5c799dad-e084-496d-8997-e9961900bf0a.png)
