# CSV To Database Insert using Mulesoft

Check my blog post - https://www.lopau.com/how-to-insert-csv-to-database-using-postgres-database-in-mulesoft/


## Create CSV sample. Using postman with raw payload
## Download and install Postgres database - https://youtu.be/-Dux6hnmWNE
## Create the table and columns
Create table and columns
```
CREATE TABLE users (    id VARCHAR(10) PRIMARY KEY,    name VARCHAR(100) NOT NULL,    created_on TIMESTAMP NOT NULL DEFAULT NOW());
```
Show tables 
```
\dt
```

## Configure the Listener and the Insert Database mule components

### Listener 
Configure the port and path
### Database
Download the JBDC driver
https://jdbc.postgresql.org/download.html

Drag the component and configure the following:
Connection: Generic Connection
https://help.mulesoft.com/s/article/Connect-to-PostgreSQL-Database
JBDC Driver: Add Maven Dependency then click Install and browse for the downloaded postgresql jar file.

Finish the configuration
URL: jdbc:postgresql://localhost:5432/csvdb
Driver class name: org.postgresql.Driver
User:
Password:

Test Connection and configure your query and test your app.
