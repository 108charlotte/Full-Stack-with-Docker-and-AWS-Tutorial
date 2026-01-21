# Authentication
Authenticating users will allow us to tie tasks to specific users and restrict the user to only add and delete tasks that are their own, which we will accomplish through both frontend and backend verification. 

**Logging in an existing user** requires a [frontend](./frontend.md) where users can enter their credentials, a [database](./database.md) to store existing accounts, and a [backend](./backend.md) to verify if the entered credentials match with any in the database. 

Similarly, **registering a new user** also requires a [frontend](./frontend.md) to enter the credentials of a new account, a [database](./database.md) to store those credentials so the user can later log in, and a [backend](./backend.md) to connect the two. 

This tutorial will follow the below structure: 
- [**Frontend**](./frontend.md): create the frontend React application with both account creation and authentication functionality
- [**Backend**](./backend.md): create the backend Django application to receive the frontend's requests and return the necessary data (uses SQLite for database as default, which will be changed in the [database](./database.md) section)
- [**Docker Compose**](./docker-compose.md): set up containers for frontend and backend with Docker Compose for simplified multi-container start-up
- [**Database**](./database.md): create Postgres database with Docker Compose file and attach to Django backend

This tutorial starts with the frontend to see Docker working and spinning up the user interface on localhost so that **issues with Docker configuration can be troubleshooted early**. Click next to get started! 