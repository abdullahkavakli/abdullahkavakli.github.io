Docker, a subset of the Moby project, is a software framework for building, running, and managing containers on servers and the cloud. The term "docker" may refer to either the tools (the commands and a daemon) or to the Dockerfile file format.

It used to be that when you wanted to run a web application, you bought a server, installed Linux, set up a LAMP stack, and ran the app. If your app got popular, you practiced good load balancing by setting up a second server to ensure the application wouldn't crash from too much traffic.

Times have changed, though, and instead of focusing on single servers, the Internet is built upon arrays of inter-dependent and redundant servers in a system commonly called "the cloud". Thanks to innovations like Linux kernel namespaces and cgroups, the concept of a server could be removed from the constraints of hardware and instead became, essentially, a piece of software. These software-based servers are called containers, and they're a hybrid mix of the Linux OS they're running on plus a hyper-localized runtime environment (the contents of the container).



Understanding containers
Container technology can be thought of as three different categories:

Builder: a tool or series of tools used to build a container, such as distrobuilder for LXC, or a Dockerfile for Docker.

Engine: an application used to run a container. For Docker, this refers to the docker command and the dockerd daemon. For others, this can refer to the containerd daemon and relevant commands (such as podman.)

Orchestration: technology used to manage many containers, including Kubernetes and OKD.

Containers often deliver both an application and configuration, meaning that a sysadmin doesn't have to spend as much time getting an application in a container to run compared to when an application is installed from a traditional source. Dockerhub and Quay.io are repositories offering images for use by container engines.

The greatest appeal of containers, though, is their ability to "die" gracefully and respawn when load balancing demands it. Whether a container's demise is caused by a crash or because it's simply no longer needed because server traffic is low, containers are "cheap" to start, and they're designed to seamlessly appear and disappear. Because containers are meant to be ephemeral and to spawn new instances as often as required, it's expected that monitoring and managing them is not done by a human in real time, but is instead automated.
