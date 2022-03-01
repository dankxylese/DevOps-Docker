# Docker
#### Common Comands
`docker run <image>` runs an image. If it doesn't find an existent image, it grabs it from the repo and downloads it.
`docker images` shows all images on the machine
`docked rm <image name or ID>` removes an image. Use `-f` if its running now
`docker login` add your credentials
`docker run -p 2368:2368 ghost` start a test website to check it works `<output on this port>:<listen on this port>`
`docker run -d -p 2368:2368 ghost` adding `-d` runs it on the background in detached mode
`docker ps -a` list images on your machine and shows if they are running