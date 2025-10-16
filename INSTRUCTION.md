1. Docker Hub Image

Full image reference: 0nira0/todoapp:1.0.0
Local tag for convenience: todoapp:1.0.0

2. Build the Docker Image

Build with Python version ARG and tags:

docker build --build-arg PYTHON_VERSION=3.8 -t todoapp:1.0.0 -t 0nira0/todoapp:1.0.0 .

3. Publish the Image

Login and push to Docker Hub:

docker login
docker push 0nira0/todoapp:1.0.0


If needed, tag locally before pushing:

docker tag todoapp:1.0.0 0nira0/todoapp:1.0.0

4. Run the Container

Run in detached mode with automatic removal:

docker run -d --rm -p 8080:8080 todoapp:1.0.0


The container runs:

python manage.py runserver 0.0.0.0:8080

5. Access the Application

Open a browser and go to:

http://localhost:8080

6. Verification Checklist

Server reachable at http://localhost:8080/

Database migrations executed during build (RUN python manage.py migrate)

ENV PYTHONUNBUFFERED=1 is set to allow live logs