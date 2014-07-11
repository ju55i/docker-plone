Plone Dockerfiles
=================

```
docker build -t ju55i/plonebase base
docker build -t ju55i/plonezeo zeo
docker build -t ju55i/ploneinstance instance

docker run --name testizeo -d -v /var/buildout/sitedata:/site ju55i/plonezeo
docker run --name testiinstance -d -v /var/buildout/sitedata:/site -p 8080:8080 --link=testizeo:zeo ju55i/ploneinstance
```
