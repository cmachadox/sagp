###### Servidor de Ativo GRUPOZAP ######
## Após realizar o gitclone, entre no diretorio e rode o comando a baixo

docker-compose up -d

## Backup 
docker exec CONTAINER /usr/bin/mysqldump -u root --password=root DATABASE > backup.sql


## Restore

cat backup.sql | docker exec -i CONTAINER /usr/bin/mysql -u root --password=root DATABASE
