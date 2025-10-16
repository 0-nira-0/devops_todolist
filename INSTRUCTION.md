My Docker Hub repository:
https://hub.docker.com/r/0nira0/todoapp

Image tag used: 1.0.0 → 0nira0/todoapp:1.0.0

Build the Docker Image

docker build -t 0nira0/todoapp:1.0.0 .

Run the Container

docker run -p 8080:8080 0nira0/todoapp:1.0.0

Access the Application

Open your browser and go to:
http://localhost:8080