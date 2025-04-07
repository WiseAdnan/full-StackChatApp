# 🧩 Full Stack Chat App - Kubernetes Manifest Deployment

This repository contains the complete set of Kubernetes manifests required to deploy a full-stack chat application, originally developed in the [iemafzalhassan/full-stack_chatApp](https://github.com/iemafzalhassan/full-stack_chatApp.git) repository. This app includes a modern frontend and a Node.js backend, connected to a MongoDB database.

I containerized the application using multi-stage Docker builds for both frontend and backend to optimize performance and image size. The Docker images were built from scratch after analyzing the original Dockerfiles and are pushed to Docker Hub for easy access and deployment.

---

All Kubernetes manifest files are placed directly in the root of this repo. No need to `cd` into any subdirectories.

## 🚀 Docker Images Used

You can directly use the following Docker images hosted on Docker Hub:

docker pull shahabadnan/chatpp-frontend:tagname
docker pull shahabadnan/chatapp-backend:tagname
You can also push them using:

docker push shahabadnan/chatpp-frontend:tagname
docker push shahabadnan/chatapp-backend:tagname
Replace tagname with the appropriate tag you have built.

How to Deploy This App
Make sure your kubectl is configured and your cluster is up.

To apply all manifests:

kubectl apply -f .
This will create and configure everything required to run the app locally on your Kubernetes setup.

Screenshots
Below are images of the chat app successfully running on localhost after deploying all manifests:

👤 User 1 View

👤 User 2 View (Incognito Window)

DevOps Highlights
✅ Used multi-stage Docker builds to reduce image size and improve security.
✅ Connected services using internal DNS within the Kubernetes cluster.
✅ Mounted persistent volume for MongoDB to retain chat data.
✅ Created ingress resource to expose the frontend on localhost.
✅ Managed secrets using Kubernetes Secrets to store credentials safely.
✅ Verified the full deployment lifecycle from build → deploy → test.

🗣 Original Project
Source Code: iemafzalhassan/full-stack_chatApp

Final Notes
This setup offers a practical full-stack Kubernetes deployment using Docker and manifests from scratch. You can modify environment variables, PVC specs, or scale replicas as per your cluster environment.

If you face any issues while deploying, make sure all required ports and ingress controllers are configured correctly.

Happy chatting!
