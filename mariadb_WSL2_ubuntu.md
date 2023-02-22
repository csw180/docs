### WSL2(Ubuntu) mariadb 설치 방법
------------------------------------
1. OS버젼 확인
```
cat /etc/os-release
```

2. Maria Site에서 제공하는 OS버젼선택 명령어 수행     
(https://mariadb.org/download/?t=repo-config&d=22.04+%22jammy%22&v=10.6&r_m=blendbyte)
```
sudo apt-get install apt-transport-https curl
sudo curl -o /etc/apt/trusted.gpg.d/mariadb_release_signing_key.asc 'https://mariadb.org/mariadb_release_signing_key.asc'
sudo sh -c "echo 'deb https://tw1.mirror.blendbyte.net/mariadb/repo/10.6/ubuntu jammy main' >>/etc/apt/sources.list"
```

3. OS update
```
sudo apt-get update
```

4. Mariadb server 설치
```
sudo apt-get install mariadb-server
..
Setting up mariadb-server-10.6 (1:10.6.11+maria~ubu2204) ...
..
```

5. Mariadb start
```
sudo service mariadb start
 * Starting MariaDB database server mariadbd       [ OK ]
```

6. MariaDB의 계정과 보안설정
```
sudo mysql_secure_installation
대부분 y 로 받아줄것
```

7. MariaDB 접속
```
sudo mysql -u root -p
123
```

* DB 접속후 참고 SQL
```
show databases;
select version();
use mysql;
select host,user,password from user;
set password for 'root'@'localhost' = PASSWORD('123');
flush privileges;
```

8. MariaDB 중지
```
sudo service mariadb stop
```