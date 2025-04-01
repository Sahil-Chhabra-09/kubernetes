## Day 1:

Containers are ephimeral, something that is short living in nature. 100 containers running on a machine get affected by each container's resource utilizations.

Problems with docker:

1. the nature of docker is scoped to _one single host_, therefore, one container can impact other
2. Lack of _auto-healing_, where without user's manual intervention, the container should start itself
3. Lack of _auto-scaling_ : as soon as the load gets increased, either you manually increase the number of container and stop them when load decreases or it should handle automatically, apart from this, we have to configure load-balancing
4. Docker is a simple platform, it does not suppot any of the enterprise level support like load-balancers, firewall, autoscaling, autoheal, api-gateways.

Kubernetes solves all of the above listed problems

By default kubernetes is a cluster, a group of nodes, it is a master node architecture. There's one master and multiple nodes.

Kubernetes has replica sets, this is what's responsible for auto-healing, it also supports something called hpa (horizontal pod autoscaler) this caters auto-scaling.

Whenever kubernetes recieves a request that the container is going down, it immediately rolls out a new container or pod (a k8s term)

kubernetes is backed up by cncf
