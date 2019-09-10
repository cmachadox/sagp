## Aplicação Controle de Stoque
### Após realizar o gitclone do repositorio, entre no diretorio e rode o comando a baixo

docker-compose up -d

### Prodecimento Backup do banco  
docker exec CONTAINER /usr/bin/mysqldump -u root --password=root DATABASE > backup.sql

### procedimento restore do banco

cat backup.sql | docker exec -i CONTAINER /usr/bin/mysql -u root --password=root DATABASE
