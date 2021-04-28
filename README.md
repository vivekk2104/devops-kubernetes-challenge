# Instructions

## Web app

1. Todo list app with react frontend, python flask backend and mysql database.

## Build

1. MySQL public image from docker hub is used for database.
2. Dockerfile for backend in backend/Dockerfile
3. Dockerfile for frontend in frontend/Dockerfile
4.  ```bash
    $ docker login -u username -p password
    $ cd backend
    $ docker build -t username/todo-backend:latest .
    $ docker push username/todo-backend:latest
    $ cd ../frontend
    $ docker build -t username/todo-frontend:latest .
    $ docker push username/todo-frontend:latest
    ```

## Run

1. Create a kubernetes cluster in cloud / local using minikube.
2. Update kubeconfig for the kubernetes cluster.
3. ```bash
   $ kubectl apply -f todo-db-deployment.yml
   $ kubectl apply -f todo-db-service.yml
   $ kubectl apply -f todo-backend-deployment.yml
   $ kubectl apply -f todo-backend-service.yml
   $ kubectl apply -f todo-frontend-deployment.yml
   $ kubectl apply -f todo-frontend-service.yml
   ```
4. Access the application at todo-frontend-service loadbalancer url
