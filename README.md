## Create postgreSQL user and database
## 1. environment and setup
(using macOS homebrew)
download the latest version of PostgreSQL:
```
 brew install postgresql
```
 check the version downloaded:
```
 postgres --version
```
## 2. PSQL
PostgreSQL can be administered from the command line using the psql utility, by running the command below:
```
 psql postgres
```
### 2.1. create user
```
 CREATE USER myuser WITH PASSWORD '123';
```
### 2.2. create database
```
 CREATE DATABASE mydb WITH OWNER myuser ENCODING = 'UTF-8';
```
## 3. PSQL in bash
### look up for the commands
```
 createuser --help
```
### 3.1. create user and set password
```
 createuser -P myuser
```

### 3.2. create user
```
 createdb mydb -O myuser
```

### 4. connect to host
```
 psql -h localhost -U myuser -d postgres -p 5432 PATH\to\filename.sql
```
