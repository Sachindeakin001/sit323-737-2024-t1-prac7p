# sit323-737-2024-t1-prac7p
This project implements a cloud-native Node.js microservice for SIT737 Task 9.1P, integrating MongoDB on a Kubernetes cluster using Docker containers. The backend code (index.js) is built with Express and Mongoose, providing RESTful CRUD endpoints (/task) to create, read, and delete task records stored in MongoDB. Environment variables such as the MongoDB URI are securely passed using Kubernetes Secrets, while the database persists data using a PersistentVolume and PVC. The application is containerized via a Dockerfile and deployed alongside MongoDB using Kubernetes Deployment and Service YAMLs. The full workflow—image build and push, secret creation, volume configuration, and resource deployment—has been tested successfully. This project satisfies all the task requirements including secure access, persistent storage, functional CRUD operations, and monitoring recommendations, and is fully documented and ready for submission.







