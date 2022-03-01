# Docker
#### Common Comands
- `docker run <image>` runs an image. If it doesn't find an existent image, it grabs it from the repo and downloads it.
- `docker images` shows all images on the machine
- `docker rm <image name or ID>` removes an image. Use `-f` if its running now
- `docker login` add your credentials
- `docker run -p 2368:2368 ghost` start a test website to check it works `<output on this port>:<listen on this port>`
- `docker run -d -p 2368:2368 ghost` adding `-d` runs it on the background in detached mode
- `docker ps -a` list images on your machine and shows if they are running
- `docker stop <processID>` to remove it

##### Connecting with SSH

- `sudo docker ps` check running processes

```
CONTAINER ID   IMAGE     COMMAND                  CREATED              STATUS              PORTS                               NAMES
47bd14bb7bc0   nginx     "/docker-entrypoint.…"   About a minute ago   Up About a minute   0.0.0.0:70->80/tcp, :::70->80/tcp   distracted_einstein
```

- grab the id
- `docker exec -it 47bd14bb7bc0 sh` to nter the shell

##### Copying files over
- `sudo docker cp index.html <dockeridfrom:dockerPS>:<Destination>`


##### Making an image
- Make a Dockerfile
```
FROM nginx
EXPOSE 80
```
- `sudo docker build -t darkxylese/test-nginx-app .`
- `sudo docker tag NginxApp darkxylese/test-nginx-app:v1`
- `sudo docker push darkxylese/test-nginx-app:v1`

- second line can be - `sudo docker tag NginxApp darkxylese/test-nginx-app:v1` depending on the name on the first command