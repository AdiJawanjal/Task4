# Swiggy Docker Deployment 🚀

This project demonstrates deploying a Dockerized web app (`adijawanjal/swiggy:latest`) using Jenkins.

## How It Works

1. Pulls image from Docker Hub
2. Removes any existing container
3. Runs the new container on port 8080

## Prerequisites

- Docker installed on Jenkins node
- Jenkins configured with necessary permissions

## Access

After pipeline runs, open:  
http://<server-ip>:8080

