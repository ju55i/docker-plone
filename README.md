Plone Dockerfiles
=================

```
docker build -t ju55i/plone-base base
docker build -t ju55i/plone-zeo zeo
docker build -t ju55i/plone-instance instance

docker run --name testzeo -d -v /var/data/site1:/buildout/var -e REPLACEME=site1 ju55i/plone-zeo
docker run --name testinstance1 -d -v /var/data/site1:/buildout/var -e REPLACEME=site1 -p 8080:8080 --link=testzeo:zeo ju55i/plone-instance
docker run --name testinstance2 -d -v /var/data/site1:/buildout/var -e REPLACEME=site1 -p 8081:8080 --link=testzeo:zeo ju55i/plone-instance
```

/var/data/site1 needs to exist in your host system. It contains the usual Plone var-directory.
