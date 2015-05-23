=====================================
A Dockerfile for Plone 4.3.4
=====================================


Build Image
==========================

$ sudo docker build -t plone434 .


Start Container
==========================

$ sudo docker run --name plone_cn -d -p 10022:22 -p 18080:8080 plone434


Access to container using SSH
================================

$ ssh -p 10022 plone@localhost


View Plone site
================================

http://localhost:18080


Mapping for local storage
================================

mapping for var folder
---------------------------

$ sudo docker run --name plone_cn -d -p 10022:22 -p 18080:8080 -v /tmp/fs/var:/home/plone/plone4_3_4/zinstance/var plone434

mapping for src folder
---------------------------

$ sudo docker run --name plone_cn -d -p 10022:22 -p 18080:8080 -v /tmp/plone_dev/src/:/home/plone/plone4_3_4/zinstance/src plone434
