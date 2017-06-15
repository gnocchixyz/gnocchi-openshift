======================
 Gnocchi on OpenShift
======================

This repository contains a Dockerfile that can be used to build an image of
Gnocchi latest version on OpenShift.

Building and pushing via Docker Hub
===================================
You can push this image on `Docker Hub <http://hub.docker.com>`_ to use it in
OpenShift later::

  $ docker build -t <username>/gnocchi
  $ docker push <username>/gnocchi

Then create an application using the image imported from the pull spec
`<username>/gnocchi`.

If you push the image after a rebuild, you can trigger a refresh of the image
if needed::

  $ oc import-image <username>/gnocchi
