## Docker commands that I use frequently

### Docker without sudo
```bash
sudo usermod -aG docker ${USER}
```

### Search images on Docker Hub
```bash
docker search image-name
```

### Download images from Docker Hub
```bash
docker pull image-name
```

### Check all the downloaded images
```bash
docker images
```

### Running a container
```bash
docker run -it container-id /bin/bash
```

### Listing all Docker containers
```bash
docker ps -a
```

### Listing active containers
```bash
docker ps
```

### Stopping a active/running container
```bash
docker stop container-id
```

### Removing a container
```bash
docker rm container-id
```
