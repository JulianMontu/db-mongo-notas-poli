# Mongo Bd contenedor de notas

# ejecutar nuestro contenedor
```
docker compose up -d
```
# como trabajar docker en una misma red

el back se debe correr con este comando:

```
docker-compose up --build
```

se debe crear una network para poder comunicar los contenedores, lo podemos hacer con el siguiente comando

```
docker network create mi_red_compartida
```

para listar las network podemos utilizar este comando:
```
docker network ls
```

Inspeccionar una red específica: Para obtener detalles sobre la red compartida (como los contenedores que están conectados a ella), usa:
```
docker network inspect mi_red_compartida
```

Verificar la conexión de un contenedor a la red: Puedes verificar si un contenedor específico está conectado a la red usando:
```
docker network inspect mi_red_compartida | grep <nombre_del_contenedor>
```