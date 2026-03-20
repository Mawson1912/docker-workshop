# Docker Workshop

This repository contains my submission for the module Cloud Infrastructure and Virtualisation (B8IS003)

The assignment involved completing the Docker Getting Started Workshop and documenting the process of building, running, and managing containerised applications.

---

## Assignment Task

> Follow the Docker Guide up to and including the deployment of multiple containers using Docker Compose.  
> Submit all sources via Git link, along with any relevant deployment links.

---

## Overview

This project documents my completion of the Docker workshop across Parts 1–7, covering:

- building Docker images  
- running and managing containers  
- updating applications  
- using bind mounts  
- persisting data with volumes  
- working with multi-container applications using Docker Compose  

Each stage of the process is documented in separate files:

- Part 1 → Part 7 (see repository file listing)

---

## Approach

I had previously worked through most of the Docker tutorial during class.  
For this assignment, I chose to work through the process again from the beginning in a clean environment.

This allowed me to:

- reinforce my understanding of each step  
- clearly document the workflow from start to finish  
- ensure that each stage of the process was captured independently  

As a result, some early steps (such as removing and recreating the application environment) reflect resetting the setup before progressing through the tutorial again.

---

## Tutorial Followed

Docker Getting Started Workshop:  
https://docs.docker.com/get-started/workshop/

---

## Relevant Links

- This repository:  
  https://github.com/Mawson1912/docker-workshop  

- Application source code (forked):  
  https://github.com/Mawson1912/getting-started-app  

- Docker Hub image:  
  https://hub.docker.com/r/donaldbs/getting-started  

---

## Repository Structure

- `Part1.md` → `Part7.md`  
  Step-by-step documentation of each stage of the Docker workshop  

- `files/`  
  Contains key configuration files used in the project:  
  - `Dockerfile`  
  - `compose.yaml`  

- `Images/`  
  Screenshots referenced throughout the documentation  

- `README.md`  
  This file  

---

## How to Use This Repository

The project is structured as a sequential walkthrough.

To review the work, please simply start at [Part 1](<Part 1.md>) and read through all parts.  

---

## Notes

This repository focuses on documenting the containerisation and orchestration process.

The application code itself is maintained separately in the linked repository, while this project captures how it is built, run, and managed using Docker.
