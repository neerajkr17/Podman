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

Codename: jammy

```
sudo apt update
```

Hit:1 http\://packages.microsoft.com/repos/code stable InRelease

Hit:2 https\://download.docker.com/linux/ubuntu jammy InRelease                 

Hit:3 https\://dl.google.com/linux/chrome/deb stable InRelease                  

Hit:4 http\://in.archive.ubuntu.com/ubuntu jammy InRelease                      

Get:5 http\://in.archive.ubuntu.com/ubuntu jammy-updates InRelease \[119 kB]     

Get:6 http\://security.ubuntu.com/ubuntu jammy-security InRelease \[110 kB]

Hit:7 http\://in.archive.ubuntu.com/ubuntu jammy-backports InRelease 

Fetched 229 kB in 2s (97.1 kB/s)

Reading package lists... Done

Building dependency tree... Done

Reading state information... Done

49 packages can be upgraded. Run 'apt list --upgradable' to see them.

N: Skipping acquire of configured file 'stable/binary-i386/Packages' as repository 'https\://download.docker.com/linux/ubuntu jammy InRelease' doesn't support architecture 'i386'

W: Target Packages (main/binary-amd64/Packages) is configured multiple times in /etc/apt/sources.list.d/google-chrome.list:3 and /etc/apt/sources.list.d/google-chrome.list:4

W: Target Packages (main/binary-all/Packages) is configured multiple times in /etc/apt/sources.list.d/google-chrome.list:3 and /etc/apt/sources.list.d/google-chrome.list:4

W: Target Translations (main/i18n/Translation-en\_IN) is configured multiple times in /etc/apt/sources.list.d/google-chrome.list:3 and /etc/apt/sources.list.d/google-chrome.list:4

W: Target Translations (main/i18n/Translation-en) is configured multiple times in /etc/apt/sources.list.d/google-chrome.list:3 and /etc/apt/sources.list.d/google-chrome.list:4

W: Target DEP-11 (main/dep11/Components-amd64.yml) is configured multiple times in /etc/apt/sources.list.d/google-chrome.list:3 and /etc/apt/sources.list.d/google-chrome.list:4

W: Target DEP-11 (main/dep11/Components-all.yml) is configured multiple times in /etc/apt/sources.list.d/google-chrome.list:3 and /etc/apt/sources.list.d/google-chrome.list:4

W: Target DEP-11-icons-small (main/dep11/icons-48x48.tar) is configured multiple times in /etc/apt/sources.list.d/google-chrome.list:3 and /etc/apt/sources.list.d/google-chrome.list:4

W: Target DEP-11-icons (main/dep11/icons-64x64.tar) is configured multiple times in /etc/apt/sources.list.d/google-chrome.list:3 and /etc/apt/sources.list.d/google-chrome.list:4

W: Target DEP-11-icons-hidpi (main/dep11/icons-64x64\@2.tar) is configured multiple times in /etc/apt/sources.list.d/google-chrome.list:3 and /etc/apt/sources.list.d/google-chrome.list:4

W: Target CNF (main/cnf/Commands-amd64) is configured multiple times in /etc/apt/sources.list.d/google-chrome.list:3 and /etc/apt/sources.list.d/google-chrome.list:4

W: Target CNF (main/cnf/Commands-all) is configured multiple times in /etc/apt/sources.list.d/google-chrome.list:3 and /etc/apt/sources.list.d/google-chrome.list:4

W: Target Packages (main/binary-amd64/Packages) is configured multiple times in /etc/apt/sources.list.d/google-chrome.list:3 and /etc/apt/sources.list.d/google-chrome.list:4

W: Target Packages (main/binary-all/Packages) is configured multiple times in /etc/apt/sources.list.d/google-chrome.list:3 and /etc/apt/sources.list.d/google-chrome.list:4

W: Target Translations (main/i18n/Translation-en\_IN) is configured multiple times in /etc/apt/sources.list.d/google-chrome.list:3 and /etc/apt/sources.list.d/google-chrome.list:4

W: Target Translations (main/i18n/Translation-en) is configured multiple times in /etc/apt/sources.list.d/google-chrome.list:3 and /etc/apt/sources.list.d/google-chrome.list:4

W: Target DEP-11 (main/dep11/Components-amd64.yml) is configured multiple times in /etc/apt/sources.list.d/google-chrome.list:3 and /etc/apt/sources.list.d/google-chrome.list:4

W: Target DEP-11 (main/dep11/Components-all.yml) is configured multiple times in /etc/apt/sources.list.d/google-chrome.list:3 and /etc/apt/sources.list.d/google-chrome.list:4

W: Target DEP-11-icons-small (main/dep11/icons-48x48.tar) is configured multiple times in /etc/apt/sources.list.d/google-chrome.list:3 and /etc/apt/sources.list.d/google-chrome.list:4

W: Target DEP-11-icons (main/dep11/icons-64x64.tar) is configured multiple times in /etc/apt/sources.list.d/google-chrome.list:3 and /etc/apt/sources.list.d/google-chrome.list:4

W: Target DEP-11-icons-hidpi (main/dep11/icons-64x64\@2.tar) is configured multiple times in /etc/apt/sources.list.d/google-chrome.list:3 and /etc/apt/sources.list.d/google-chrome.list:4

W: Target CNF (main/cnf/Commands-amd64) is configured multiple times in /etc/apt/sources.list.d/google-chrome.list:3 and /etc/apt/sources.list.d/google-chrome.list:4

W: Target CNF (main/cnf/Commands-all) is configured multiple times in /etc/apt/sources.list.d/google-chrome.list:3 and /etc/apt/sources.list.d/google-chrome.list:4

```
sudo apt-get install podman
```

Reading package lists... Done

Building dependency tree... Done

Reading state information... Done

The following packages were automatically installed and are no longer required:

  gyp libc-ares2 libjs-events libjs-highlight.js libjs-inherits libjs-is-typedarray libjs-psl libjs-source-map libjs-sprintf-js libjs-typedarray-to-buffer libnode-dev libnode72 libssl-dev libuv1-dev

  node-abbrev node-ansi-regex node-ansi-styles node-ansistyles node-are-we-there-yet node-arrify node-asap node-asynckit node-balanced-match node-brace-expansion node-chownr node-clean-yaml-object

  node-color-convert node-color-name node-commander node-core-util-is node-decompress-response node-delayed-stream node-delegates node-depd node-diff node-encoding node-end-of-stream node-err-code

  node-escape-string-regexp node-fancy-log node-foreground-child node-fs.realpath node-function-bind node-get-stream node-glob node-growl node-has-flag node-has-unicode node-hosted-git-info node-iconv-lite

  node-iferr node-imurmurhash node-indent-string node-inflight node-inherits node-ini node-ip node-ip-regex node-is-buffer node-is-plain-obj node-is-typedarray node-isarray node-isexe

  node-json-parse-better-errors node-jsonparse node-kind-of node-lodash-packages node-lowercase-keys node-lru-cache node-mimic-response node-minimatch node-minimist node-minipass node-mute-stream

  node-negotiator node-npm-bundled node-once node-osenv node-p-cancelable node-p-map node-path-is-absolute node-process-nextick-args node-promise-inflight node-promise-retry node-promzard node-pump

  node-quick-lru node-read node-readable-stream node-resolve node-retry node-safe-buffer node-set-blocking node-signal-exit node-slash node-slice-ansi node-source-map node-spdx-correct node-spdx-exceptions

  node-spdx-expression-parse node-spdx-license-ids node-sprintf-js node-stealthy-require node-string-decoder node-supports-color node-text-table node-time-stamp node-tmatch node-typedarray-to-buffer

  node-universalify node-util-deprecate node-validate-npm-package-license node-webidl-conversions node-whatwg-fetch node-wrappy node-yallist nodejs-doc

Use 'sudo apt autoremove' to remove them.

The following additional packages will be installed:

  buildah catatonit conmon containernetworking-plugins crun fuse-overlayfs golang-github-containernetworking-plugin-dnsname golang-github-containers-common golang-github-containers-image libostree-1-1 uidmap

Suggested packages:

  containers-storage docker-compose

The following NEW packages will be installed:

  buildah catatonit conmon containernetworking-plugins crun fuse-overlayfs golang-github-containernetworking-plugin-dnsname golang-github-containers-common golang-github-containers-image libostree-1-1 podman

  uidmap

0 upgraded, 12 newly installed, 0 to remove and 49 not upgraded.

Need to get 25.3 MB of archives.

After this operation, 109 MB of additional disk space will be used.

Do you want to continue? \[Y/n] y

Get:1 http\://in.archive.ubuntu.com/ubuntu jammy-updates/universe amd64 uidmap amd64 1:4.8.1-2ubuntu2.1 \[22.4 kB]

Get:2 http\://in.archive.ubuntu.com/ubuntu jammy/universe amd64 golang-github-containers-image all 5.16.0-3 \[29.3 kB]

Get:3 http\://in.archive.ubuntu.com/ubuntu jammy/universe amd64 golang-github-containers-common all 0.44.4+ds1-1 \[28.1 kB]

Get:4 http\://in.archive.ubuntu.com/ubuntu jammy/universe amd64 libostree-1-1 amd64 2022.2-3 \[333 kB]

Get:5 http\://in.archive.ubuntu.com/ubuntu jammy/universe amd64 buildah amd64 1.23.1+ds1-2 \[6,094 kB]                                                                                                              

Get:6 http\://in.archive.ubuntu.com/ubuntu jammy/universe amd64 catatonit amd64 0.1.7-1 \[307 kB]                                                                                                                   

Get:7 http\://in.archive.ubuntu.com/ubuntu jammy/universe amd64 conmon amd64 2.0.25+ds1-1.1 \[35.1 kB]                                                                                                              

Get:8 http\://in.archive.ubuntu.com/ubuntu jammy/universe amd64 containernetworking-plugins amd64 0.9.1+ds1-1 \[6,422 kB]                                                                                           

Get:9 http\://in.archive.ubuntu.com/ubuntu jammy/universe amd64 crun amd64 0.17+dfsg-1.1 \[300 kB]                                                                                                                  

Get:10 http\://in.archive.ubuntu.com/ubuntu jammy/universe amd64 fuse-overlayfs amd64 1.7.1-1 \[44.7 kB]                                                                                                            

Get:11 http\://in.archive.ubuntu.com/ubuntu jammy/universe amd64 golang-github-containernetworking-plugin-dnsname amd64 1.3.1+ds1-2 \[1,083 kB]                                                                     

Get:12 http\://in.archive.ubuntu.com/ubuntu jammy-updates/universe amd64 podman amd64 3.4.4+ds1-1ubuntu1.22.04.2 \[10.6 MB]                                                                                         

Fetched 25.3 MB in 22s (1,134 kB/s)                                                                                                                                                                               

Selecting previously unselected package uidmap.

(Reading database ... 224016 files and directories currently installed.)

Preparing to unpack .../00-uidmap\_1%3a4.8.1-2ubuntu2.1\_amd64.deb ...

Unpacking uidmap (1:4.8.1-2ubuntu2.1) ...

Selecting previously unselected package golang-github-containers-image.

Preparing to unpack .../01-golang-github-containers-image\_5.16.0-3\_all.deb ...

Unpacking golang-github-containers-image (5.16.0-3) ...

Selecting previously unselected package golang-github-containers-common.

Preparing to unpack .../02-golang-github-containers-common\_0.44.4+ds1-1\_all.deb ...

Unpacking golang-github-containers-common (0.44.4+ds1-1) ...

Selecting previously unselected package libostree-1-1:amd64.

Preparing to unpack .../03-libostree-1-1\_2022.2-3\_amd64.deb ...

Unpacking libostree-1-1:amd64 (2022.2-3) ...

Selecting previously unselected package buildah.

Preparing to unpack .../04-buildah\_1.23.1+ds1-2\_amd64.deb ...

Unpacking buildah (1.23.1+ds1-2) ...

Selecting previously unselected package catatonit.

Preparing to unpack .../05-catatonit\_0.1.7-1\_amd64.deb ...

Unpacking catatonit (0.1.7-1) ...

Selecting previously unselected package conmon.

Preparing to unpack .../06-conmon\_2.0.25+ds1-1.1\_amd64.deb ...

Unpacking conmon (2.0.25+ds1-1.1) ...

Selecting previously unselected package containernetworking-plugins.

Preparing to unpack .../07-containernetworking-plugins\_0.9.1+ds1-1\_amd64.deb ...

Unpacking containernetworking-plugins (0.9.1+ds1-1) ...

Selecting previously unselected package crun.

Preparing to unpack .../08-crun\_0.17+dfsg-1.1\_amd64.deb ...

Unpacking crun (0.17+dfsg-1.1) ...

Selecting previously unselected package fuse-overlayfs.

Preparing to unpack .../09-fuse-overlayfs\_1.7.1-1\_amd64.deb ...

Unpacking fuse-overlayfs (1.7.1-1) ...

Selecting previously unselected package golang-github-containernetworking-plugin-dnsname.

Preparing to unpack .../10-golang-github-containernetworking-plugin-dnsname\_1.3.1+ds1-2\_amd64.deb ...

Unpacking golang-github-containernetworking-plugin-dnsname (1.3.1+ds1-2) ...

Selecting previously unselected package podman.

Preparing to unpack .../11-podman\_3.4.4+ds1-1ubuntu1.22.04.2\_amd64.deb ...

Unpacking podman (3.4.4+ds1-1ubuntu1.22.04.2) ...

Setting up crun (0.17+dfsg-1.1) ...

Setting up uidmap (1:4.8.1-2ubuntu2.1) ...

Setting up libostree-1-1:amd64 (2022.2-3) ...

Setting up golang-github-containers-image (5.16.0-3) ...

Setting up conmon (2.0.25+ds1-1.1) ...

Setting up containernetworking-plugins (0.9.1+ds1-1) ...

Setting up catatonit (0.1.7-1) ...

Setting up golang-github-containernetworking-plugin-dnsname (1.3.1+ds1-2) ...

Setting up fuse-overlayfs (1.7.1-1) ...

Setting up golang-github-containers-common (0.44.4+ds1-1) ...

Setting up buildah (1.23.1+ds1-2) ...

Setting up podman (3.4.4+ds1-1ubuntu1.22.04.2) ...

Created symlink /etc/systemd/user/default.target.wants/podman.service → /usr/lib/systemd/user/podman.service.

Created symlink /etc/systemd/user/sockets.target.wants/podman.socket → /usr/lib/systemd/user/podman.socket.

Created symlink /etc/systemd/system/default.target.wants/podman.service → /lib/systemd/system/podman.service.

Created symlink /etc/systemd/system/sockets.target.wants/podman.socket → /lib/systemd/system/podman.socket.

Created symlink /etc/systemd/system/default.target.wants/podman-auto-update.service → /lib/systemd/system/podman-auto-update.service.

Created symlink /etc/systemd/system/timers.target.wants/podman-auto-update.timer → /lib/systemd/system/podman-auto-update.timer.

Created symlink /etc/systemd/system/default.target.wants/podman-restart.service → /lib/systemd/system/podman-restart.service.

Processing triggers for libc-bin (2.35-0ubuntu3.4) ...

Processing triggers for man-db (2.10.2-1) ...

neeraj\@neeraj-G3-3500:\~$ 

podman info

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

podman version

Version:      3.4.4

API Version:  3.4.4

Go Version:   go1.18.1

Built:        Thu Jan  1 05:30:00 1970

OS/Arch:      linux/amd64


# To Search for a image in registry<a id="to-search-for-a-image-in-registry"></a>

Podman search nginx

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


# To run an image<a id="to-run-an-image"></a>

podman run docker.io/library/ngnix

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


# How to Create our own image?<a id="how-to-create-our-own-image"></a>

Create a python file named app.py and add following line 

print(“Hello Neeraj!”)

Run our python program using

Python3 app.py

Create a new directory

mkdir myimage

cd myimage

neeraj\@neeraj-G3-3500:\~$ pwd

/home/neeraj

neeraj\@neeraj-G3-3500:\~$ mkdir myimage

neeraj\@neeraj-G3-3500:\~$ cd myimage/

neeraj\@neeraj-G3-3500:\~/myimage$ touch app.py

neeraj\@neeraj-G3-3500:\~/myimage$ ls

app.py

neeraj\@neeraj-G3-3500:\~/myimage$ vi app.py

neeraj\@neeraj-G3-3500:\~/myimage$ cat app.py

print ("Hey Neeraj!")

neeraj\@neeraj-G3-3500:\~/myimage$ python3 -V

Python 3.10.12

neeraj\@neeraj-G3-3500:\~/myimage$ python3 app.py

Hey Neeraj!

Create a Podmanfile

neeraj\@neeraj-G3-3500:\~/myimage$ python3 -V

Python 3.10.12

neeraj\@neeraj-G3-3500:\~/myimage$ python3 app.py

Hey Neeraj!

neeraj\@neeraj-G3-3500:\~/myimage$ touch Podmanfile

neeraj\@neeraj-G3-3500:\~/myimage$ ls

app.py  Podmanfile

neeraj\@neeraj-G3-3500:\~/myimage$ vi Podmanfile

neeraj\@neeraj-G3-3500:\~/myimage$ cat Podmanfile

FROM python:3.10.2

WORKDIR /app

COPY . .

CMD \["python", "app.py"]

To build an image

podman build -t myimage:1.1 .
