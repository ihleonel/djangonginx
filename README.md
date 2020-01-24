# Django - Gunicorn - Nginx - Docker
En este projecto se expone una configuración básica para la integración de nginx y gunicorn sobre contenedores docker.

## Dependencias
1. git
1. docker
1. docker-compose


## Iniciar
Primero se deberán iniciar todos los servicios. Iniciamos el nginx-proxy
```bash
docker-compose -f docker-compose-proxy up
```
Iniciamos la aplicación prod
```bash
docker-compose -f docker-compose-prod up
```
Iniciamos la aplicación test
```bash
docker-compose -f docker-compose-test up
```
Para probar cada sitio
```bash
curl -H "Host: sitio.local" localhost
```
```bash
curl -H "Host: test.sitio.local" localhost
```