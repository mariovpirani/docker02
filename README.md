# docker02
Aula 01
https://github.com/mariovpirani/docker01

#### AULA 02<br /><br />

### LINUX<br />
##### ONDE ESTA /Documentos/Impacta trocar por seu caminho<br />
docker run -d -v $(pwd)/Documentos/IMPACTA/docker/services/db/data:/var/lib/mysql --rm --name mysql-container mysql-image<br /><br />
### Abrindo a porta para acesso<br />
docker run -d -v $(pwd)/Documentos/IMPACTA/docker/services/db/data:/var/lib/mysql -p 3306:3306 --rm --name mysql-container mysql-image<br /><br />
<hr>

### WINDOWS<br />
##### Onde está o D:/estudos/faculdade/docker/docker02 trocar por seu caminho<br />
docker run -d -v D:/estudos/faculdade/docker/docker02/services/db/data:/var/lib/mysql --rm --name mysql-container mysql-image<br /><br />

### Abrindo a porta para acesso<br />
docker run -d -v D:/estudos/faculdade/docker/docker02/services/db/data:/var/lib/mysql -p 3306:3306 --rm --name mysql-container mysql-image<br /><br />

### Roda Script sql<br />
docker exec -i mysql-container mysql -uroot -pimpacta < services/db/script.sql<br /><br />

### Acessa o Container<br />
docker exec -it mysql-container /bin/bash<br /><br />

### Acessar o Mysql <br />
mysql -uroot -pimpacta<br /><br />


### MYSQL<br />
show databases;<br />
use IMPACTA_DATABASE;<br />
show tables;<br />
SELECT * FROM CLIENTE;<br />


### Para acessar via dbeaver apos subir a instância<br />
###### Aba Main<br />
<strong>Server</strong><br />
Server host: localhost<br />
Port: 3306<br />
Database: IMPACTA_DATABASE<br /><br />

<strong>Authentication</strong><br />
username: root<br />
password: impacta

