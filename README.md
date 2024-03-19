Login to mySQL: 
Root: docker exec -it mysql_server mysql -u root -p

User: docker exec -it mysql_server mysql -D snippetbox -u web -p

ALTER the datauser 'web' and also grant priviledges for the correct ip address: 
GRANT SELECT, INSERT, UPDATE, DELETE ON snippetbox.* TO 'web'@'localhost';
-- Important: Make sure to swap 'pass' with a password of your own choosing.
ALTER USER 'web'@'localhost' IDENTIFIED BY 'pass';

Change "localhost" to the IP that you are connecting from. 

Create a self-signed TLS certificate: 
$ cd $HOME/PATH_TO_GO_PROJECT
$ mkdir tls
$ cd tls

 
