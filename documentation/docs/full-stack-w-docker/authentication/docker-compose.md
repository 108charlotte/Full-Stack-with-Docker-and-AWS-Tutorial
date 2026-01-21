# Docker Compose
Although the frontend and backend ran successfully, it required **four Docker commands** to run. What if this whole process could be consolidated into a **single command**? 

Docker Compose lets you do exactly that by using a `docker-compose.yaml` file. Simply running **`docker compose up --build` can accomplish everything the previous commands could** and with **less room for human error**. 

First, create a `docker-compose.yaml` file at the root of the repository (it should be a sibling to `backend` and `frontend`). Then, add the following: 

```dockerfile
services: 
  backend: 
    # defines the location of the backend's Dockerfile
    build: ./backend
    # sets the port for the backend container and connects the container's port 8000 with your local device's port 8000 so you can access it over localhost
    ports: 
      - "8000:8000"
    # creates a sync between local backend folder and app folder - running container will update immediately based on changes
    volumes:
      - ./backend:/app

  frontend: 
    # defines the location of the frontend's Dockerfile
    build: ./frontend
    # sets the port for the frontend container and connects the container's port 5173 with your local device's port 5173 so you can access it over localhost
    ports: 
      - "5173:5173"
```

Now try it out! First, we have to stop the frontend and backend containers. You can do this by going to Docker desktop and stopping the running frontend and backend containers! You can also delete them to remove clutter, since we won't be using them anymore. 

Run `docker compose up` in the directory with your `docker-compose.yaml` file (use `ls` to make sure you're in the right place) and go to `http://localhost:5173/register`. Your old account you created won't exist anymore since the containers have changed, but you can try out making a new account - everything should work the same as when you ran 4 commands, but now in only one! If you ever need to force the containers to rebuild, you can do so by adding the `--build` flag to the end of `docker compose up`. Now, you'll learn how to set up a PostgreSQL database using Docker Compose! 