## Development Environment in Docker

### Purpose
Keeping development environment same at work, home, etc. easily by building docker container. Also you can pull ready container from hub.docker.com, too.

### Installation

Pull docker image and run it.

```
deniz@machine~$ sudo docker pull denizeren/devenv
deniz@machine~$ sudo docker run -d -P --privileged --name devenv denizeren/devenv
deniz@machine~$ sudo docker port devenv 22
0.0.0.0:49154
deniz@machine~$ ssh root@localhost -p 49154
```

or build from scratch

```bash
deniz@machine~$ git clone https://github.com/denizeren/devenv.git
deniz@machine~$ cd devenv
deniz@machine~$ sudo docker build -t devenv .
deniz@machine~$ sudo docker run -d -P --privileged --name devenv devenv
deniz@machine~$ docker port devenv 22
0.0.0.0:49154
deniz@machine~$ ssh root@localhost -p 49154
```

Default login credentials:
```
root:deniz
```
