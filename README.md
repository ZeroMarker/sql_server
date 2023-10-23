# sql_server

docker run -e "ACCEPT_EULA=Y" -e "MSSQL_SA_PASSWORD=password" -e "MSSQL_PID=Evaluation" -p 1433:1433  --name sqlpreview --hostname sqlpreview -d mcr.microsoft.com/mssql/server

docker exec -it sqlpreview /opt/mssql-tools/bin/sqlcmd -S localhost -U sa -P password