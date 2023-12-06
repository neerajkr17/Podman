![](https://lh7-us.googleusercontent.com/NXF1lcSjd9AiM_Uh9RFp0t3t-bGCF5sxJEyoXBpaXEqnoD9Rn25cgxeO0Q4hmsDXnXfuGvqKrSLabwAeFlZq40_nxs6E2YiRYQdBisJ8X30dCxxSZPDqYZ9mXUqH8Xz6C8qSQtpVLRESD7JHyajo1t0)


# What is Podman?<a id="what-is-podman"></a>

- Podman provides a secure and lightweight alternative to docker for creating and managing containers on Linux systems.

- Podman allows you to package an application and its dependencies into a single container that can run anywhere without any dependency on the host system.


# Why Podman? (Features of Podman)<a id="why-podman-features-of-podman"></a>

- Daemonless:- Podman does not require background daemon to run, make it more lightweight and efficient than Docker.

* Rootless Containers:- To run PODMAN containers, root privileges are not required.

- Multi-Container Application:- Podman supports running multiple containers as part of an application, and it provides tools for managing and connecting these containers.

* More Secure:- Podman launches each container with a security enhanced linux(SELinux) label and its rootless feature makes it more secure.


# What are Pods?<a id="what-are-pods"></a>

Pods are a group of containers that run together and share the same resources.


# Containers<a id="containers"></a>

A container is a lightweight, portable, and self-sufficient unit that can run applications and their dependencies. Containers package the application code, runtime, libraries, and other necessary components into a single unit. They run on a shared operating system kernel and isolate the application processes from each other and from the host system. Popular containerization platforms include Docker and container orchestration tools like Kubernetes.


# Step for Installation:-<a id="step-for-installation-"></a>

## Prerequisite<a id="prerequisite"></a>
```
lsb\_release -a
```

No LSB modules are available.

Distributor ID: Ubuntu

Description: Ubuntu 22.04.3 LTS

Release: 22.04


```
sudo apt update
```

```
sudo apt-get install podman
```

```
podman info
```

```
podman version
```

Version:      3.4.4

API Version:  3.4.4

Go Version:   go1.18.1

Built:        Thu Jan  1 05:30:00 1970

OS/Arch:      linux/amd64


# To Search for a image in registry<a id="to-search-for-a-image-in-registry"></a>
```
Podman search nginx
```

NAME                                                                   DESCRIPTION

registry.fedoraproject.org/f29/nginx                                   

registry.fedoraproject.org/f29/origin-nginx-router                     

registry.access.redhat.com/ubi8/nginx-120                              Platform for running nginx 1.20 or building...

registry.access.redhat.com/ubi8/nginx-118                              Platform for running nginx 1.18 or building...

registry.access.redhat.com/ubi9/nginx-120                              rhcc\_registry.access.redhat.com\_ubi9/nginx-1...

registry.access.redhat.com/ubi8/nginx-122                              rhcc\_registry.access.redhat.com\_ubi8/nginx-1...

registry.access.redhat.com/ubi9/nginx-122                              rhcc\_registry.access.redhat.com\_ubi9/nginx-1...

registry.access.redhat.com/rhscl/nginx-18-rhel7                        Nginx 1.8 server and a reverse proxy server

registry.access.redhat.com/rhscl/nginx-112-rhel7                       Nginx is a web server and a reverse proxy se...

registry.access.redhat.com/rhscl/nginx-114-rhel7                       Nginx is a web server and a reverse proxy se...

registry.access.redhat.com/rhscl/nginx-110-rhel7                       Nginx container image that delivers an nginx...

registry.access.redhat.com/rhscl/nginx-16-rhel7                        Nginx 1.6 server and a reverse proxy server

registry.access.redhat.com/ubi7/nginx-118                              Platform for running nginx 1.18 or building...

registry.access.redhat.com/ubi7/nginx-120                              Platform for running nginx 1.20 or building...

registry.access.redhat.com/3scale-amp23/apicast-gateway                3scale's API gateway (APIcast) is an OpenRe...

registry.access.redhat.com/3scale-amp20/apicast-gateway                3scale's API gateway (APIcast) is an OpenRes...

registry.access.redhat.com/rhamp10/apicast-gateway                     3scale's API gateway (APIcast) is an OpenRes...

registry.access.redhat.com/3scale-amp20-beta/apicast-gateway           3scale's API gateway (APIcast) is an OpenRes...

registry.access.redhat.com/3scale-amp25/apicast-gateway                3scale's API gateway (APIcast) is an OpenRes...

registry.access.redhat.com/3scale-amp21/apicast-gateway                3scale AMP image used for API gateway

registry.access.redhat.com/3scale-amp24/apicast-gateway                No description

registry.access.redhat.com/rhmap45/wildcard-proxy                      RHMAP image that provides mapping and proxy...

registry.access.redhat.com/rhmap46/wildcard-proxy                      RHMAP image that provides mapping and proxy...

registry.access.redhat.com/rhmap47/wildcard-proxy                      RHMAP image that provides mapping and proxy...

registry.access.redhat.com/rhmap44/wildcard-proxy                      RHMAP Docker image that provides mapping and...

registry.access.redhat.com/rhmap43/wildcard-proxy                      RHMAP Docker image that provides mapping and...

registry.access.redhat.com/3scale-amp22/apicast-gateway                APIcast API gateway needs connection to the...

quay.io/kubernetes-ingress-controller/nginx-ingress-controller         NGINX Ingress controller built around the \[K...

quay.io/openshift-scale/nginx                                          

quay.io/ukhomeofficedigital/nginx-proxy                                # OpenResty Docker Container  \[!\[Build Statu...

quay.io/centos7/nginx-116-centos7                                      Nginx is a web server and a reverse proxy se...

quay.io/jitesoft/nginx                                                 # N \[!\[Docker Pulls]\(https\://img.shie...

quay.io/cloud-bulldozer/nginx                                          

quay.io/bedrock/nginx                                                  

quay.io/martinhelmich/prometheus-nginxlog-exporter                     Export metrics from Nginx access log files t...

quay.io/redhattraining/hello-world-nginx                               

quay.io/olmqe/nginxolm-operator-bundle                                 

quay.io/giantswarm/ingress-nginx-controller                            

quay.io/ocsci/nginx                                                    

quay.io/libpod/alpine\_nginx                                            This image is used for testing purposes only...

quay.io/olmqe/nginxolm-operator-index                                  

quay.io/telco5gci/nginx                                                

quay.io/centos7/nginx-114-centos7                                      Nginx is a web server and a reverse proxy se...

quay.io/aptible/nginx                                                  !\[]\(https\://quay.io/repository/aptible/nginx...

quay.io/openshifttest/nginx-alpine                                     

quay.io/nginx/nginx-ingress                                            

quay.io/astronomer/ap-nginx                                            

quay.io/astronomer/ap-nginx-es                                         

quay.io/domino/kubernetes-ingress-controller.nginx-ingress-controller  

quay.io/dtan4/nginx-basic-auth-proxy                                   

quay.io/olmqe/nginx-ok-index                                           

quay.io/nginx/nginx-prometheus-exporter

Checking already downloaded images

Podman images

REPOSITORY                     TAG         IMAGE ID      CREATED       SIZE

docker.io/library/hello-world  latest      9c7a54a9a43c  7 months ago  19.9 kB

To download an image

Podman pull 

Trying to pull docker.io/library/nginx:latest...

Getting image source signatures

Copying blob 84b1ff10387b done  

Copying blob 9ea27b074f71 done  

Copying blob 9a59d19f9c5b done  

Copying blob 9b16c94bb686 done  

Copying blob 1f7ce2fa46ab done  

Copying blob c6edf33e2524 done  

Copying blob 517357831967 done  

Copying config a6bd71f48f done  

Writing manifest to image destination

a6bd71f48f6839d9faae1f29d3babef831e76bc213107682c5cc80f0cbb30866

```
sudo mkdir -p /etc/apt/keyrings
curl -fsSL "https://download.opensuse.org/repositories/devel:kubic:libcontainers:unstable/xUbuntu_$(lsb_release -rs)/Release.key" \
  | gpg --dearmor \
  | sudo tee /etc/apt/keyrings/devel_kubic_libcontainers_unstable.gpg > /dev/null
echo \
  "deb [arch=$(dpkg --print-architecture) signed-by=/etc/apt/keyrings/devel_kubic_libcontainers_unstable.gpg]\
    https://download.opensuse.org/repositories/devel:kubic:libcontainers:unstable/xUbuntu_$(lsb_release -rs)/ /" \
  | sudo tee /etc/apt/sources.list.d/devel:kubic:libcontainers:unstable.list > /dev/null
sudo apt-get update -qq
sudo apt-get -qq -y install podman
```
```
sudo apt install curl
```

# To run an image<a id="to-run-an-image"></a>

```
podman run docker.io/library/ngnix
```


/docker-entrypoint.sh: /docker-entrypoint.d/ is not empty, will attempt to perform configuration

/docker-entrypoint.sh: Looking for shell scripts in /docker-entrypoint.d/

/docker-entrypoint.sh: Launching /docker-entrypoint.d/10-listen-on-ipv6-by-default.sh

10-listen-on-ipv6-by-default.sh: info: Getting the checksum of /etc/nginx/conf.d/default.conf

10-listen-on-ipv6-by-default.sh: info: Enabled listen on IPv6 in /etc/nginx/conf.d/default.conf

/docker-entrypoint.sh: Sourcing /docker-entrypoint.d/15-local-resolvers.envsh

/docker-entrypoint.sh: Launching /docker-entrypoint.d/20-envsubst-on-templates.sh

/docker-entrypoint.sh: Launching /docker-entrypoint.d/30-tune-worker-processes.sh

/docker-entrypoint.sh: Configuration complete; ready for start up

2023/12/05 09:05:27 \[notice] 1#1: using the "epoll" event method

2023/12/05 09:05:27 \[notice] 1#1: nginx/1.25.3

2023/12/05 09:05:27 \[notice] 1#1: built by gcc 12.2.0 (Debian 12.2.0-14) 

2023/12/05 09:05:27 \[notice] 1#1: OS: Linux 6.2.0-37-generic

2023/12/05 09:05:27 \[notice] 1#1: getrlimit(RLIMIT\_NOFILE): 1048576:1048576

2023/12/05 09:05:27 \[notice] 1#1: start worker processes

2023/12/05 09:05:27 \[notice] 1#1: start worker process 24

2023/12/05 09:05:27 \[notice] 1#1: start worker process 25

2023/12/05 09:05:27 \[notice] 1#1: start worker process 26

2023/12/05 09:05:27 \[notice] 1#1: start worker process 27

2023/12/05 09:05:27 \[notice] 1#1: start worker process 28

2023/12/05 09:05:27 \[notice] 1#1: start worker process 29

2023/12/05 09:05:27 \[notice] 1#1: start worker process 30

2023/12/05 09:05:27 \[notice] 1#1: start worker process 31


# To run an image in a background <a id="to-run-an-image-in-a-background"></a>

podman run -d docker.io/library/ngnix

c837732dfcae57a664533ff99e9c7d51a9040035e4f74041b6095d7a85628182


# To see the running containers<a id="to-see-the-running-containers"></a>

Podman ps

CONTAINER ID  IMAGE                           COMMAND               CREATED         STATUS         PORTS       NAMES

c837732dfcae  docker.io/library/nginx:latest  nginx -g daemon o...  47 seconds ago  Up 47 seconds              sad\_bhaskara

neeraj\@neeraj-G3-3500:\~$ ifconfig

docker0: flags=4099\<UP,BROADCAST,MULTICAST>  mtu 1500

        inet 172.17.0.1  netmask 255.255.0.0  broadcast 172.17.255.255

        ether 02:42:f9:c1:d2:37  txqueuelen 0  (Ethernet)

        RX packets 0  bytes 0 (0.0 B)

        RX errors 0  dropped 0  overruns 0  frame 0

        TX packets 0  bytes 0 (0.0 B)

        TX errors 0  dropped 0 overruns 0  carrier 0  collisions 0

enp59s0: flags=4099\<UP,BROADCAST,MULTICAST>  mtu 1500

        ether 34:73:5a:d4:fe:8c  txqueuelen 1000  (Ethernet)

        RX packets 0  bytes 0 (0.0 B)

        RX errors 0  dropped 0  overruns 0  frame 0

        TX packets 0  bytes 0 (0.0 B)

        TX errors 0  dropped 0 overruns 0  carrier 0  collisions 0

lo: flags=73\<UP,LOOPBACK,RUNNING>  mtu 65536

        inet 127.0.0.1  netmask 255.0.0.0

        inet6 ::1  prefixlen 128  scopeid 0x10\<host>

        loop  txqueuelen 1000  (Local Loopback)

        RX packets 12669  bytes 1213093 (1.2 MB)

        RX errors 0  dropped 0  overruns 0  frame 0

        TX packets 12669  bytes 1213093 (1.2 MB)

        TX errors 0  dropped 0 overruns 0  carrier 0  collisions 0

wlp0s20f3: flags=4163\<UP,BROADCAST,RUNNING,MULTICAST>  mtu 1500

        inet 192.168.1.13  netmask 255.255.255.0  broadcast 192.168.1.255

        inet6 fe80::b0a:1781:29ce:9369  prefixlen 64  scopeid 0x20\<link>

        ether b4:0e:de:b5:91:90  txqueuelen 1000  (Ethernet)

        RX packets 889920  bytes 913549480 (913.5 MB)

        RX errors 0  dropped 0  overruns 0  frame 0

        TX packets 264559  bytes 119118796 (119.1 MB)

        TX errors 0  dropped 0 overruns 0  carrier 0  collisions 0

![](https://lh7-us.googleusercontent.com/00OaRcyYAkmOt737ht48-wmNafRqMaU0zOlkoT47BqM--joqeLQo21ICepxsJuLIpesQEqax6eq9Vgyin9S_Vuw2O0tf16l0YiHizKkEvorGZJd-XtfXjeXfUKPH1e4COojdNSdhnWojveHZqE6r-Kg)


# Port Binding of container<a id="port-binding-of-container"></a>

podman run -dt -p 8080:80/tcp docker.io/library/nginx

Fd4ec00e7222ac3b2d9f9b94da9135f5ff503001e3a50f433629d439655f5d39

neeraj\@neeraj-G3-3500:\~$ podman ps

CONTAINER ID  IMAGE                           COMMAND               CREATED         STATUS         PORTS                 NAMES

c837732dfcae  docker.io/library/nginx:latest  nginx -g daemon o...  12 minutes ago  Up 12 minutes                        sad\_bhaskara

fd4ec00e7222  docker.io/library/nginx:latest  nginx -g daemon o...  23 seconds ago  Up 22 seconds  0.0.0.0:8080->80/tcp  festive\_liskov

![](https://lh7-us.googleusercontent.com/u1zQAx3JW0VxI49bchpGN8rmHOycKpU1lU_TnSaL3MwagtrWoryL8daUb9yEDVCLt5Ag8A2o4tIa4iz88VEMjsQC4UU5Us0EvjKHG7AY4S8cWB7fAx9zsV65MVNENXay1XbGJ6m9SJ5U3ykA4qP1ZFk)


# To Stop a container<a id="to-stop-a-container"></a>

podman stop \<container\_name / container id>

neeraj\@neeraj-G3-3500:\~$ podman stop c837732dfcae

c837732dfcae


# To run multiple containers with different port<a id="to-run-multiple-containers-with-different-port"></a>

podman run -dt -p 8081:80/tcp docker.io/library/nginx

podman run -dt -p 8082:80/tcp docker.io/library/nginx


# To see all the existing containers<a id="to-see-all-the-existing-containers"></a>

Podman ps -a


# To remove the existing containers<a id="to-remove-the-existing-containers"></a>

podman rm \<container\_name>

