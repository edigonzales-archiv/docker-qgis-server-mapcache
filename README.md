# docker-qgis-server-mapcache
Docker image w/ QGIS server and MapCache 

```
docker build -t sogis/qgis-server-mapcache .
```

```
docker run -p 8281:80 --rm --name qgis-server-mapcache sogis/qgis-server-mapcache
docker run -p 8281:80 -v /Users/stefan/Projekte/qwc2-background-layer-seeding/vagrant/background-layer-seeder:/geodata/geodata --rm --name qgis-server-mapcache sogis/qgis-server-mapcache
```

```
bash -c "clear && docker exec -it qgis-server-mapcache /bin/bash"
```

## Search/Replace datasources in qgs file

```
/vagrant/
/geodata/geodata/
```

```
source="dbname='pub' host=localhost port=5432 user='ddluser'
source="service='sogis_services'
```

```
<datasource>dbname='pub' host=localhost port=5432 user='ddluser' password='ddluser'
<datasource>service='sogis_services'
```

## TODO
- Maske (BBOX) in Datenbank.