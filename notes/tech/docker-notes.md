

attaching to a stopped (?) container:

`docker start <unique id>`

`docker attach <unique id>`

After that second command:tab, your terminal prompt should've changed.

---

Running a new container:

`docker run -it ubuntu /bin/bash`

This will run the container in interactive mode and start a bash prompt. 
- `-i` is for interactive.
- `-t` is to assign a tty.
- `-d` runs it in detached mode, so in the  background.

---

Pulling an image so you can use it later/again from the main repo

`docker pull -a fedora`

the `-a` flag will pull all versions

---

Look at the currently installed containers

`docker ps -a`

`-a` will show us all the installed ones. Without it, it will just show the running ones.

---

Exit from a tty: `ctrl+p` then `ctrl+c` but leave it running

---

`docker images` shows all downloaded images.

--- 

Making and exporting an image

`docker commit <id> <image name>` will create your own image.

`docker save -o <dest.tar> <image name>` will save the image (large).

`docker load -e <src.tar>` will load an image into your docker

`docker run -it <loaded image name> /bin/bash` will open an interactive bash like we've seen before

---

Container workflows

When running interactively, you can detach from the container by `ctrl+p ctrl+c`.  This will leave it running in the background.

`docker stop <container id>` sends SIGTERM to PID1

`docker start <container id>` starts up the last running process for that container

`docker attach <container id>` puts you back in interactive mode

`docker restart <container id>` SIGTERMs PID1 and starts it back up, I think.

---

Deleting Containers

`docker info` shows number of images and containers

`docker rm <container id>` removes container

---

Container information

`docker top <container id>` shows all running processes

`docker inspect <container id>` shows json information about a running container.

--- 

Connecting to container

`docker inspect <container id> | grep Pid` gives us the host's pid for a container

`nsenter -m -u -n -p -i -t <pid> /bin/bash` changes namespaces

Namespaces: mount, uts, network, process, ipc of -target pid.

`docker-enter <container id>`

`docker exec -it <container id> /bin/bash`: recommended
