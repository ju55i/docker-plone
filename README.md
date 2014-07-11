Plone Dockerfiles
=================

```
docker build -t ju55i/plonebase base
docker build -t ju55i/plonezeo zeo
docker build -t ju55i/ploneinstance instance

docker run --name testzeo -d -v /var/buildout/sitedata:/site ju55i/plonezeo
docker run --name testinstance1 -d -v /var/buildout/sitedata:/site -p 8080:8080 --link=testzeo:zeo ju55i/ploneinstance
docker run --name testinstance2 -d -v /var/buildout/sitedata:/site -p 8081:8080 --link=testzeo:zeo ju55i/ploneinstance
```
