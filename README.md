
## Dev
1. Clonar Repositorio
2. Crear un archivo `.env`  basado en `.env.template`
3. Reconstruir los submodulos ejecutando el comantdo `git submodule update --init --recursive`
4. Construir ejecuntando el comando `docker compose up --build`


## Pasos para crear los Git Submodules
1. Crear un nuevo repositorio en GitHub
2. Clonar el repositorio en la máquina local
3. Añadir el submodule, repository_url es el url del repositorio de la rama main y directorio_name es el nombre de repositorio.
```
git submodule add <repository_url> <directory_name>
```
Ejm
```
git submodule add https://github.com/Xpoch-Ticket/nest-client-gateway.git nest-client-gateway
```
4. Añadir los cambios al repositorio (git add, git commit, git push)
Ej:
```
git add .
git commit -m "Add submodule"
git push
```


## Comando adicionales 
1. Inicializar y actualizar Sub-módulos, cuando alguien clona el repositorio por primera vez, debe de ejecutar el siguiente comando para inicializar y actualizar los sub-módulos
```
git submodule update --init --recursive
```
1. Para actualizar las referencias de los sub-módulos
```
git submodule update --remote
```




## PRODUCTION

1. Clonar el repositorio
2. Crear un .env basado en el .env.template
3. Ejecutar el comando

```
docker compose -f docker-compose.prod.yml build
```