![](https://lh7-us.googleusercontent.com/WddWh5XDjHfSIO_pwEtwGKTX10GPOLdHiDJ05E99G9Gp6cgJKUQuj4i4qDAGB7b2j9X07-jkTi2dyaJRP46xajbb-D7u9g1Bgoy3XIPepPpp6gqs4UF502cn5l9PztYxUb8WLSHN5hfyR389pShu9tI)

# Table of Contents
   - [What is Podman?](#what-is-podman)
   - [Why Podman? (Features of Podman)](#why-podman-features-of-podman)
   - [What are Pods?](#what-are-pods)
   - [Containers](#containers)
   - [Steps for Installation](#step-for-installation-)
   - [Prerequisite](#prerequisite)
   - [Installation Commands](#installation-commands)
   - [Checking Podman Version](#checking-podman-version)
   - [Additional Installations](#additional-installations)
   - [Searching for Images](#to-search-for-a-image-in-registry)
   - [Downloading an Image](#to-download-an-image)
   - [Checking Downloaded Images](#checking-already-downloaded-images)
   - [Running an Image in the Background](#to-run-an-image-in-a-background)
   - [Viewing Running Containers](#to-see-the-running-containers)
   - [Port Binding of Container](#port-binding-of-container)
   - [Stopping a Container](#to-stop-a-container)
   - [Running Multiple Containers with Different Ports](#to-run-multiple-containers-with-different-port)
   - [Viewing All Existing Containers](#to-see-all-the-existing-containers)
   - [Removing Existing Containers](#to-remove-the-existing-containers)
   - [Removing an Image](#to-remove-image)
  
     
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

Codename: jammy

```
sudo apt update
```

```
sudo apt-get install podman
```

```
podman info
```


host:

  arch: amd64

  buildahVersion: 1.23.1

  cgroupControllers:

  - memory

  - pids

  cgroupManager: systemd

  cgroupVersion: v2

  conmon:

    package: 'conmon: /usr/bin/conmon'

    path: /usr/bin/conmon

    version: 'conmon version 2.0.25, commit: unknown'

  cpus: 8

  distribution:

    codename: jammy

    distribution: ubuntu

    version: "22.04"

  eventLogger: journald

  hostname: neeraj-G3-3500

  idMappings:

    gidmap:

    - container\_id: 0

      host\_id: 1000

      size: 1

    - container\_id: 1

      host\_id: 100000

      size: 65536

    uidmap:

    - container\_id: 0

      host\_id: 1000

      size: 1

    - container\_id: 1

      host\_id: 100000

      size: 65536

  kernel: 6.2.0-37-generic

  linkmode: dynamic

  logDriver: journald

  memFree: 694177792

  memTotal: 8100720640

  ociRuntime:

    name: crun

    package: 'crun: /usr/bin/crun'

    path: /usr/bin/crun

    version: |-

      crun version 0.17

      commit: 0e9229ae34caaebcb86f1fde18de3acaf18c6d9a

      spec: 1.0.0

      +SYSTEMD +SELINUX +APPARMOR +CAP +SECCOMP +EBPF +YAJL

  os: linux

  remoteSocket:

    path: /run/user/1000/podman/podman.sock

  security:

    apparmorEnabled: false

    capabilities: CAP\_CHOWN,CAP\_DAC\_OVERRIDE,CAP\_FOWNER,CAP\_FSETID,CAP\_KILL,CAP\_NET\_BIND\_SERVICE,CAP\_SETFCAP,CAP\_SETGID,CAP\_SETPCAP,CAP\_SETUID,CAP\_SYS\_CHROOT

    rootless: true

    seccompEnabled: true

    seccompProfilePath: /usr/share/containers/seccomp.json

    selinuxEnabled: false

  serviceIsRemote: false

  slirp4netns:

    executable: /usr/bin/slirp4netns

    package: 'slirp4netns: /usr/bin/slirp4netns'

    version: |-

      slirp4netns version 1.0.1

      commit: 6a7b16babc95b6a3056b33fb45b74a6f62262dd4

      libslirp: 4.6.1

  swapFree: 2146430976

  swapTotal: 2147479552

  uptime: 10h 52m 59.29s (Approximately 0.42 days)

plugins:

  log:

  - k8s-file

  - none

  - journald

  network:

  - bridge

  - macvlan

  volume:

  - local

registries: {}

store:

  configFile: /home/neeraj/.config/containers/storage.conf

  containerStore:

    number: 0

    paused: 0

    running: 0

    stopped: 0

  graphDriverName: overlay

  graphOptions: {}

  graphRoot: /home/neeraj/.local/share/containers/storage

  graphStatus:

    Backing Filesystem: extfs

    Native Overlay Diff: "true"

    Supports d\_type: "true"

    Using metacopy: "false"

  imageStore:

    number: 0

  runRoot: /run/user/1000/containers

  volumePath: /home/neeraj/.local/share/containers/storage/volumes

version:

  APIVersion: 3.4.4

  Built: 0

  BuiltTime: Thu Jan  1 05:30:00 1970

  GitCommit: ""

  GoVersion: go1.18.1

  OsArch: linux/amd64

  Version: 3.4.4

```
podman version
```


Version:      3.4.4

API Version:  3.4.4

Go Version:   go1.18.1

Built:        Thu Jan  1 05:30:00 1970

OS/Arch:      linux/amd64


## If curl is not installed on your machine.<a id="if-curl-is-not-installed-on-your-machine"></a>

```
sudo apt install curl
```


## If you're not able to search any image then run this command.<a id="if-youre-not-able-to-search-any-image-then-run-this-command"></a>

```
sudo mkdir -p /etc/apt/keyrings

curl -fsSL "https\://download.opensuse.org/repositories/devel:kubic:libcontainers:unstable/xUbuntu\_$(lsb\_release -rs)/Release.key" \\

  | gpg --dearmor \\

  | sudo tee /etc/apt/keyrings/devel\_kubic\_libcontainers\_unstable.gpg > /dev/null

echo \\

  "deb \[arch=$(dpkg --print-architecture) signed-by=/etc/apt/keyrings/devel\_kubic\_libcontainers\_unstable.gpg]\\

    https\://download.opensuse.org/repositories/devel:kubic:libcontainers:unstable/xUbuntu\_$(lsb\_release -rs)/ /" \\

  | sudo tee /etc/apt/sources.list.d/devel:kubic:libcontainers:unstable.list > /dev/null

sudo apt-get update -qq

sudo apt-get -qq -y install podman
```

## To Search for a image in registry<a id="to-search-for-a-image-in-registry"></a>

```
Podman search nginx
```


## To download an image<a id="to-download-an-image"></a>

```
podman pull docker.io/library/nginx:latest
```


## Checking already downloaded images<a id="checking-already-downloaded-images"></a>

```
Podman images
```

REPOSITORY                     TAG         IMAGE ID      CREATED       SIZE

docker.io/library/hello-world  latest      9c7a54a9a43c  7 months ago  19.9 kB


## To run an image in a background <a id="to-run-an-image-in-a-background"></a>

```
podman run -d docker.io/library/ngnix
```

c837732dfcae57a664533ff99e9c7d51a9040035e4f74041b6095d7a85628182


## To see the running containers<a id="to-see-the-running-containers"></a>

```
Podman ps
```

## Port Binding of container<a id="port-binding-of-container"></a>

```
podman run -dt -p 8080:80/tcp docker.io/library/nginx
```

Run it on web browser

<http://localhost:8080/>

![](https://lh7-us.googleusercontent.com/W-fuwAyG8cqRjvTLUD6cAVlY1XLNS2ZUzXKQcM3i8zqnffKWcfGYRI85r4R3ouNytacWp1LWRO-NPhIwL_gR91SfeeEo2TK0ufGsAlJ4SUxzstQ45oY-YKW18f-GKEeWQEGmKc0DtpooSfH4Dss2vGE)


# To Stop a container<a id="to-stop-a-container"></a>

```
podman stop \<container\_name / container id>
```

## To run multiple containers with different port<a id="to-run-multiple-containers-with-different-port"></a>


podman run -dt -p 8081:80/tcp docker.io/library/nginx

podman run -dt -p 8082:80/tcp docker.io/library/nginx


## To see all the existing containers<a id="to-see-all-the-existing-containers"></a>

```
Podman ps -a
```

## To remove the existing containers<a id="to-remove-the-existing-containers"></a>

```
podman rm f \<container\_name>
```

## To remove image<a id="to-remove-image"></a>

```
podman images
```
```
podman rmi -f docker.io/library/nginx 
```
