# Docker Workshop

This repository documents my completion of the Docker Getting Started Workshop for my Cloud Infrastructure and Virtualisation assignment.

The aim of the project was to demonstrate the basics of Docker, including:

- building images
- running containers
- updating applications
- persisting data with volumes
- using bind mounts
- deploying multiple containers with Docker Compose

## Tutorial Followed

Docker Getting Started Workshop:  
https://docs.docker.com/get-started/workshop/

## Relevant Links

Forked application repository:  
https://github.com/Mawson1912/getting-started-app

Docker Hub image:  
https://hub.docker.com/r/donaldbs/getting-started

## Overview

The application used in this project is the Docker tutorial todo app.

I first worked through the Docker tutorial during term. For this assignment, I created this separate clean repository to present the process clearly and to reinforce my understanding by working through the steps again.

## Stages Completed

### 1. Build and run a Docker image

A Dockerfile was used to package the application into a Docker image.

Example commands:

```bash
docker build -t getting-started .
docker run -d -p 8080:3000 getting-started# docker-workshop
This repository documents my completion of the Docker Getting Started Workshop for my Cloud Infrastructure and Virtualisation assignment.
