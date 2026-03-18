# Part 3 – Sharing the Application

## Overview

In this section, the Docker Getting Started tutorial demonstrates how to share a container image by pushing it to Docker Hub.

This allows the application to be stored remotely and accessed from other environments, enabling easier deployment and collaboration.

---

## Implementation

I already completed this step during Part 1 of this assignment, perhaps slightly jumping the gun.

As part of the initial setup, the Docker image was tagged and pushed to Docker Hub using the following commands:

```bash
docker tag getting-started donaldbs/getting-started
docker push donaldbs/getting-started
```

This uploaded the image to my Docker Hub repository, making it available for reuse and deployment.

---

## Evidence

The same screenshots provided in Part 1 demonstrate this process:

![Docker push](Images/10%20Pushing%20container%20image%20to%20docker%20hub.png)

![Docker dashboard](Images/11%20Container%20image%20in%20docker%20hub.png)

---

## Key Learnings

This section reinforces the importance of container registries in a containerised workflow. By pushing images to Docker Hub:

- applications can be shared across different machines and environments  
- deployments become more flexible and portable  
- images can be versioned and reused efficiently  

This step forms the bridge between local development and real-world deployment scenarios.
