# Learn Docker

Learn Docker is an interactive tutorial for learning Docker commands and usage patterns by going through series for example cases.
All the cases are written in [Jupyter Notebook](http://jupyter.org/) so that you can run real Docker commands in the browser
based learning environment which is ideal for beginners.

## Install

The tutorial is already been packed into a [Docker image](https://hub.docker.com/r/tryk8s/learn-docker/). You can launch it in your
preferred Docker environment.

### Docker

```
docker run -v /var/run/docker.sock:/var/run/docker.sock -p 8888:8888 tryk8s/learn-docker
```

In order to accomplish the tutorial, you also have to run a [Docker registry](https://docs.docker.com/registry/) at `localhost:5000`
which is needed in one case.

```
docker run -p 127.0.0.1:5000:5000 registry:2
```

Then you could visit `http://$SERVER_IP:8888` in your browser to start the tutorial.


### Kubernetes

Launch this tutorial in Kubernetes is very easy

```
kubectl create -f https://raw.githubusercontent.com/tryk8s/learn-docker/master/manifests/learn-docker-rc.yaml
kubectl create -f https://raw.githubusercontent.com/tryk8s/learn-docker/master/manifests/learn-docker-notebook-svc.yaml
```

This just create the Replication Controller and Service needed. You can then visit `http://$NODE_IP:30888` in your browser to start the tutorial.


### TryK8S

The easiest way to launch this tutorial is using [TryK8S](http://tryk8s.com). We have already made it as an cluster addon.
You can simply deploy it with one click and begin to learn Docker right away.

## License

MIT
