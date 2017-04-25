# ppoffice/apache-php-mssql-odbc
Dockerfile of Apache & PHP Environment with Microsoft SQL Server ODBC Driver Support Built on Ubuntu Trusty

```bash
docker pull ppoffice/apache-php-mssql-odbc
```

## Build
```bash
docker build -t ppoffice/apache-php-mssql-odbc .
```

## Running
```bash
docker run -d -p 80:80 ppoffice/apache-php-mssql-odbc
```
With custom `www` folder:
```bash
docker run -d -p 5000:80 -v /home/eduardo/Sites/www-xpert:/var/www/ ppoffice/apache-php-mssql-odbc
```

## Docker Commands

#### List all processes
```bash
sudo docker ps -a -q
```

#### Stop all processes
```bash
docker stop NAME_PROCESSES
```

#### Remove all processes
```bash
docker rm NAME_PROCESSES
```

## Other
Uncomment these two lines in Dockerfile to fix "non-UTF8" chars encoding and time format problems:
```bash
ADD freetds.conf /etc/freetds/
ADD locales.conf /etc/freetds/
```

## Issues
[https://github.com/ppoffice/apache-php-mssql-odbc/issues](https://github.com/ppoffice/apache-php-mssql-odbc/issues)
