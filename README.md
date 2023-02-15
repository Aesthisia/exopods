## Exopods: Container Management and Logging


Made with 🧡 by [Aesthisia](https://www.linkedin.com/company/aesthisia)

New age web based container management &amp; logging platform for developers.

Exopods is a platform for containerization and management of applications. This logging platform aims to simplify the process of managing and monitoring Docker containers and their logs.

Current version `rc-1.0.01` is a alpha release, You might encounter some issues. We have already listed the know issues if you are facing any other issues, feel free to raise an issue in this repo.

## Features

- Easy management of Docker containers.
- Real-time logging for Docker containers.
- Search and filter logs by container, image, and time.
- Automatic rotation and archival of logs.
- Multiple methods for integrating logs into external systems such as Elasticsearch or Logstash.

## Getting Started

To get started with exopods platform, you need to have a basic understanding of Docker and its containers. You also need to have Docker installed on your system.
Note: Currently exopods support only linux/amd64 based os images. 

### Prerequisites

- Docker
- Docker Compose(optional)

## Installation

Before starting the container make sure you change the `HOST_URL`, it should be same as the host, in which you will be accessing the exopods. For example: if you are using ec2 linux, use public ip as host url, `http://xx.xxx.xx.xx:8001`

### Deploy on docker host


```
sudo docker run -d \
  -v /var/run/docker.sock:/var/run/docker.sock \
  -e "HOST_URL=http://localhost:8001" \
  --name exopods \
  -p 80:8001 \
  aesthisia/exopods:rc-1.0.01
```

### Deploy on docker-compose

Clone the repo or copy & create a docker-compose.yaml & paste the content from the file present in this repo. Also make sure to change the `HOST_URL` in docker-compose.yml. 

```
sudo docker-compose up -d
```


Navigate to the host url & you will be redirected to the login page. Also make sure desired port is open & not being blocked by your firewall. 


### Usage

The logging platform provides an intuitive web interface for managing and monitoring Docker containers and their logs. You can perform the following tasks:

- View a list of all containers and their status.
- Start, stop, and restart containers(To be added)
- View logs for a specific container in real-time.
- Search and filter logs by container, image, and time.(To be added)

## Version

This is an Alpha release, `rc-1.0.01` available on [Dockerhub](https://hub.docker.com/repository/docker/aesthisia/exopods/general).


## Docker Resources

Here are some resources to help you learn more about Docker:

- [Docker Documentation](https://docs.docker.com/)
- [Docker Compose Documentation](https://docs.docker.com/compose/)
- [Docker Hub](https://hub.docker.com/)

## Known Issues

Some of the known issue & temporary fix:

- Refresh page might not work in some cases, go back to `HOST_URL` to restart your session.
- Log window may look hovering over the screen in case of high res screens. 
- If container list doesn't shows up first time then close the session & re-login again or go back to `HOST_URL`.

If you are facing any other issues, please raise a issue request or send us email at info@aesthisia.com.


## Links

Linkedin: [https://www.linkedin.com/company/aesthisia](https://www.linkedin.com/company/aesthisia)

Website: [https://aesthisia.com/](https://aesthisia.com/)

Github: [https://github.com/Aesthisia](https://github.com/Aesthisia)

Dockerhub: [https://hub.docker.com/repository/docker/aesthisia/exopods/general](https://hub.docker.com/repository/docker/aesthisia/exopods/general)

