# sql_server

sudo docker pull mcr.microsoft.com/mssql/server:2022-latest

sudo docker run -e "ACCEPT_EULA=Y" -e "MSSQL_SA_PASSWORD=<YourStrong@Passw0rd>" \
   -p 1433:1433 --name sql1 --hostname sql1 \
   -d \
   mcr.microsoft.com/mssql/server:2022-latest

docker run -e "ACCEPT_EULA=Y" -e "MSSQL_SA_PASSWORD=Passw0rd" -p 1433:1433  --name sqlpreview --hostname sqlpreview -d mcr.microsoft.com/mssql/server:2022-latest

docker exec -it sqlpreview /opt/mssql-tools/bin/sqlcmd -S localhost -U sa -P password