# docker-sistel
Dockerfile e afins do container do sistel 

## Como rodar

1. docker build .

2. docker run -it --name sistel -p 80:8080 -e ENVDB=$ENVDB -e USERDB=$USERDB -e PASSDB=$PASSDB -e USERLDAP=$USERLDAP -e PASSLDAP=$PASSLDAP -v DIRETORIO-WAR:/opt/jboss/wildfly/standalone/deployments/ IDIMAGEM

Obs: as variáveis de ambiente acima precisam ser definidas, ENVDB = host do banco de dados

## Conexão com bancos

Atualmente estamos adicionando um host local.db que aponta para outro container com o banco de dados, para mudar o ip basta editar o arquivos src/addHosts.sh

## Log

localização do log dentro do container: /opt/jboss/wildfly/standalone/log/server.log
