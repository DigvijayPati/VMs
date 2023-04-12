# spin-off ubuntu 20.04 minimal VM & install docker inside it

### A) Install vagrant & virtualbox on your local machine (host machine)

### B) Create Vagrantfile

Use pre-built base VM box available on Vagrant cloud

https://github.com/geerlingguy/packer-boxes/tree/master/ubuntu2004 

https://app.vagrantup.com/geerlingguy/boxes/ubuntu2004
```bash
$ geerlingguy/ubuntu2004  

```

Vagrantfile automatically downloads this box on your local machine from Vagrant cloud. 


### C) Start the VM
```bash
$ vagrant up 

```

### D) If you modify the VM
```bash
$ vagrant reload --provision

```

### D) ssh into the VM and run docker 
```bash
$ vagrant ssh

```

```bash
Welcome to Ubuntu 20.04.3 LTS (GNU/Linux 5.4.0-42-generic x86_64)

 * Documentation:  https://help.ubuntu.com
 * Management:     https://landscape.canonical.com
 * Support:        https://ubuntu.com/advantage
Failed to connect to https://changelogs.ubuntu.com/meta-release-lts. Check your Internet connection or proxy settings

Last login: Wed Apr 12 19:08:39 2023 from 10.0.2.2
vagrant@build-linux-vm-1:~$

```


```bash
 
vagrant@build-linux-vm-1:~$ docker run hello-world
Unable to find image 'hello-world:latest' locally
latest: Pulling from library/hello-world
2db29710123e: Pull complete
Digest: sha256:4e83453afed1b4fa1a3500525091dbfca6ce1e66903fd4c01ff015dbcb1ba33e
Status: Downloaded newer image for hello-world:latest

Hello from Docker!
This message shows that your installation appears to be working correctly.

vagrant@build-linux-vm-1:~$ docker images
REPOSITORY    TAG       IMAGE ID       CREATED         SIZE
hello-world   latest    feb5d9fea6a5   18 months ago   13.3kB
vagrant@build-linux-vm-1:~$ 

```


### D) Check the status of VM
```bash
$ vagrant status

```

```bash
Current machine states:

build-linux-vm-1   running (virtualbox)

```

