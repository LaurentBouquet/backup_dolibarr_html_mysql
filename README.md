# backup_dolibarr_html_mysql

## Docker run

docker run -d --name demo-dolibarr-backup --hostname demo-backup --link demo-mariadb --restart=always -v demo_dolibarr_html:/var/www/html -v demo_dolibarr_docs:/var/www/documents -v demo_dolibarr_custom:/var/www/html/custom -v demo_dolibarr_conf:/var/www/html/conf -v /etc/localtime:/etc/localtime:ro -v /home/backup:/backup -e "MYSQL_ROOT_PASSWORD=aSecurePassword" -e "MYSQL_DATABASE=dolibarr" -e "DOLIBARR_CONTAINER_NAME=demo-dolibarr" -e "MYSQL_CONTAINER_NAME=demo-mariadb" lbouquet/backup_dolibarr_html_mysql:latest crond -f -d 8 

## Docker compose

TODO

