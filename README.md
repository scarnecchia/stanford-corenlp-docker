stanford-corenlp-docker
=======================

This Dockerfile will build and run the most current release of the
[Stanford CoreNLP server](http://stanfordnlp.github.io/CoreNLP/corenlp-server.html) in a docker container.

Usage
=====

To download and run a [prebuilt version of the CoreNLP server](https://hub.docker.com/r/mountainherder/corenlp/)
from Docker Hub locally at ``http://localhost:9000``, just type:

```
docker run -p 9000:9000 mountainherder/corenlp
```

By default, CoreNLP will use up to 8GB of RAM. You can change this by setting
the `JAVA_XMX` environment variable. Here, we're giving it 3GB:

```
docker run -e JAVA_XMX=3g -p 9000:9000 -ti corenlp-docker
```

Forked from nlpbox/corenlp