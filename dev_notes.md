# dev notes

## find port usage and kill it

```bash

netstat -ano | findstr :yourPortNumber

taskkill /pid yourid /f

```

## docker

docker clean:

@echo off
FOR /f "tokens=*" %%i IN ('docker ps -aq') DO docker rm %%i
FOR /f "tokens=*" %%i IN ('docker images --format "{{.ID}}"') DO docker rmi %%i
