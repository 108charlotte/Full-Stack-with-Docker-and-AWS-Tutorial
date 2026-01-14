# Full Stack with Docker: Section Overview
This part of the tutorial is an introduction to deploying a full-stack todo list containerized with Docker, which in the second part will be deployed on AWS EC2 instances. The frontend will use **React**, the backend will use **Django**, and the database will use **PostgreSQL**. 

:::tip
Don't go install all of these right now! Docker will allow you to run React, Django, Postgres, and many more technologies without having them installed locally on your machine through **containerization**
:::

Development will be divided into three sections: 
* **[User Authentication](./authentication/authentication.md)**: allowing users to login and register
* **[Tasks](./tasks/tasks.md)**: allowing authenticated users to view, add, and delete tasks
* **[Permissions](./permissions/permissions.md)**: limiting users permissions to only add and delete tasks that belong to them

Each section will include an overview file named after the section (ex. "Authentication", "Tasks", "Permissions"), a section on setting up the frontend for that specific section, and a section on setting up the backend for that section. 

Click next to get started with authentication! 