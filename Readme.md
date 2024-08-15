**User Data to Install Docker**

```
#!/bin/bash
sudo yum update -y
sudo yum install -y yum-utils
sudo yum-config-manager --add-repo https://download.docker.com/linux/rhel/docker-ce.repo
sudo yum install docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin
sudo systemctl start docker
sudo systemctl enable docker
sudo usermod -aG docker ec2-user
```


## Docker Cheat Sheet
### Docker Images
- **Build an image from a Dockerfile:**
  ```bash
  docker build -t <image_name> .
  ```
- **List local images:**
  ```bash
  docker images
  ```
- **Delete an image:**
  ```bash
  docker rmi <image_name>
  ```

### Docker Containers
- **Run a container:**
  ```bash
  docker run --name <container_name> <image_name>
  ```
- **Run a container in the background:**
  ```bash
  docker run -d <image_name>
  ```
- **List running containers:**
  ```bash
  docker ps
  ```
- **Stop a container:**
  ```bash
  docker stop <container_name>
  ```
- **Remove a stopped container:**
  ```bash
  docker rm <container_name>
  ```

### Docker Hub
- **Login to Docker Hub:**
  ```bash
  docker login -u <username>
  ```
- **Push an image to Docker Hub:**
  ```bash
  docker push <username>/<image_name>
  ```
- **Pull an image from Docker Hub:**
  ```bash
  docker pull <image_name>
  ```

## Contributing
If you would like to contribute to this project, please follow these steps:
1. Fork the repository.
2. Create a new branch (`git checkout -b feature-branch`).
3. Make your changes.
4. Commit your changes (`git commit -m 'Add new feature'`).
5. Push to the branch (`git push origin feature-branch`).
6. Create a new Pull Request.

