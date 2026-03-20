# Part 1 – Containerising the Application

## Overview

In this section, I followed the Docker "Getting Started" tutorial to containerise and run a simple Node.js todo application.

Unlike the default tutorial setup, this was completed on a Google Cloud virtual machine, meaning Docker was running remotely rather than on my local machine.

---

## Steps

### 1. Connecting to the VM

I connected to the Ubuntu VM using:

```bash
gcloud compute ssh vm01 --zone=europe-west2-c
```

![Running VM](Images/01%20Running%20VM.png)

---

### 2. Preparing the application

The tutorial application was set up inside the VM environment and prepared for containerisation.

![Preparing app](Images/02%20Removing%20and%20creating%20app%20in%20VM.png)

---

### 3. Creating the Dockerfile

A Dockerfile was created to define how the image should be built:

```dockerfile
FROM node:24-alpine
WORKDIR /app
COPY . .
RUN npm install --omit=dev
CMD ["node", "src/index.js"]
EXPOSE 3000
```

![Dockerfile added](Images/03%20Dockerfile%20added.png)

---

### 4. Building the container image

The image was built using:

```bash
docker build -t getting-started .
```

This downloaded the base image and installed the application dependencies.

![Building container image](Images/04%20Building%20container%20image.png)

---

### 5. Running the container

The container was started with port mapping:

```bash
docker run -d -p 8080:3000 getting-started
```

Port 3000 inside the container was mapped to port 8080 on the VM.

![Start container](Images/05%20Start%20an%20app%20container.png)

---

### 6. Accessing the application

Because the container was running on a VM, I used SSH tunnelling to access it in the browser:

```bash
gcloud compute ssh vm01 --zone=europe-west2-c -- -L 8080:localhost:8080
```

![SSH tunnel](Images/06%20SSH%20tunnel%20to%20see%20app%20in%20my%20browser.png)

---

### 7. Verifying the application

The application was successfully accessed in the browser and tested by adding items.

![App running](Images/07%20The%20app%20running%20in%20browser.png)

![Items added](Images/08%20The%20app%20running%20in%20browser%20items%20added.png)

![Confirmation](Images/09%20Confirmation%20container%20is%20running%20as%20it%20should.png)

---

### 8. Pushing image to Docker Hub

The image was tagged and pushed to Docker Hub:

```bash
docker tag getting-started donaldbs/getting-started
docker push donaldbs/getting-started
```

![Push to Docker Hub](Images/10%20Pushing%20container%20image%20to%20docker%20hub.png)

![Docker Hub image](Images/11%20Container%20image%20in%20docker%20hub.png)

---

## Key Learning

* Docker allows applications to be packaged with all dependencies into portable containers
* A Dockerfile defines how an image is built
* Port mapping connects container ports to external access
* Running Docker on a VM introduces an additional networking layer compared to local development
* Docker Hub can be used to store and share container images

[Continue to next part](<Part 2.md>)
