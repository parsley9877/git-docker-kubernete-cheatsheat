# git-cheatsheet

* `git init` --> initialize local repo
* `git remote add <remote_name> <ssh key of remote>`
* `git add <files>`
* `git commit -m <message>`
* `git push <remote name> <remote branch>`
* `git pull <remote name> <remote branch>`
* `git branch -m <new name>` --> rename current branch
* `git rm -r <file name> `--> to add an already removed file
* `git rm -f PATH` --> unstages already added path or file

# docker-cheatsheat
* always run the docker daemon first
* `docker pull REMOTE_IMAGE` --> pulling remote image file to local .kube
* `docker images` --> see all local image files
* `docker run LOCAL_IMAGE SHELL_COMMAND` --> run continers and exec SHELL_COMMAND in it, then exits.
* `docker ps -a` --> all running containers
* `docker run -it LOCAL_IMAGE sh` --> generate ann interactive run of image, useful for executing multiple commands
* `docker rm CONTAINER_ID` --> remove container
* `docker rm $(docker ps -a -q -f status=exited)` --> deletes all exited containers. -a get ids, -f filters based on the condition
* `docker run --rm IMAGE` --> automatically delete container after exiting it
* `docker rmi IMAGE_FILE` --> for removing images
* `docker run -d -P --name static-site prakhar1989/static-site` --> it runs the image in detached mode (-d: without dpeendence on terminal), and publish (-P) all container ports to random ports
* `docker port [CONTAINER]` --> see published ports of the container
* `docker stop CONTINER_ID` --> to stop a detached conntainer
* `docker run -p 8888:80 prakhar1989/static-site` --> custom port binding (-p)
