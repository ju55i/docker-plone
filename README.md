Plone Dockerfiles
=================

Install [docker-compose](http://docs.docker.com/compose/). Type docker-compose up and point your browser to localhost. Both the user and password are admin.

You can also run things manually as follows:
```
docker build -t ju55i/plone-base base
docker build -t ju55i/plone-zeo zeo
docker build -t ju55i/plone-instance instance
docker build -t ju55i/plone-varnish varnish

docker run --name testzeo -d -v ~/Data/zope-var:/buildout/var -e REPLACEME=site1 ju55i/plone-zeo
docker run --name testinstance1 -d -v ~/Data/zope-var:/buildout/var -e REPLACEME=site1 -p 8080:8080 --link=testzeo:zeo ju55i/plone-instance
docker run --name testinstance2 -d -v ~/Data/zope-var:/buildout/var -e REPLACEME=site1 -p 8081:8080 --link=testzeo:zeo ju55i/plone-instance
docker run --name testvarnish -p 80:6081 --link=testinstance1:instance1 --link=testinstance2:instance2 ju55i/plone-varnish
```

~/Data/zope-var needs to exist in your host system. It contains the usual Plone var-directory. You can set it up also in docker-compose.yml using volumes definition. Remember that uids are inherited to container when mounting a volume. This setup expects that uid 65 has read-write permissions to the volume.
