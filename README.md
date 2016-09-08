# docker-mysql-phpmyadmin
docker-mysql-phpmyadmin with local volumn

git clone https://github.com/tung1404/docker-mysql-phpmyadmin.git

cd docker-mysql-phpmyadmin

Build image from Dockerfile: 
docker build -t mysql:local .

Modyfy docker-compose.yml, 
db.volumns: 
/Users/tung1404/Documents/docker/movacal/data:/var/lib/mysql:rw
- /Users/tung1404/Documents/docker/movacal/data : change to folder's path where store DB file

Run on normal: docker-compose up
Run on deamon: docker-compose up -d 

Connect mysql by command: ./mysql -h 192.168.99.100 -P 13306 -uroot -ppassword
- host(192.168.99.100) 
- port(13306)
- user: root
- user's password: password (specify in Dockerfile)
