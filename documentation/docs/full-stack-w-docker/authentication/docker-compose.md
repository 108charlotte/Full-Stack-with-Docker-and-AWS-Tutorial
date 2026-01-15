# Docker Compose
Although the frontend and backend ran successfully, it required four different Docker commands to run. What if this whole process could be consolidated into a single command? 

Docker compose lets you do exactly that by using a docker-compose.yaml file. Simply running `docker compose up --build` can accomplish everything the previous four commands could and with less room for human error. 

First, create a "docker-compose.yaml" file at the root of the repository (it should be a sibling to "backend" and "frontend"). Then, add the following: 

```dockerfile
services: 
  backend: 
    build: ./backend
    ports: 
      - "8000:8000"
    # creates a sync between local backend folder and app folder - running container will update immediately based on changes
    volumes:
      - ./backend:/app

  frontend: 
    build: ./frontend
    ports: 
      - "5173:5173"
```