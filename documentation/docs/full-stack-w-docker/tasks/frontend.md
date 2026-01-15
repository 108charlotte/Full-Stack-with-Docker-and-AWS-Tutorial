# Frontend
Go into the "frontend" folder, then into "src" and find `App.jsx`. It will have some placeholder content, including a vite logo and React logo. Delete this content to create a base to work from, including the imports we will be using:  

```jsx
import { useState, useEffect } from 'react'; 
import './App.css'; 
import { useLocation } from 'react-router-dom'; // this is the only difference from the authentication pages; it will be used to get the current user's username, which is passed from login and registration
import { getCookie } from './csrftoken.jsx'; 
import { useNavigate } from 'react-router-dom'; 

function App() {

  return (
    <>
      
    </>
  )
}

export default App; 
```

## Setting Variables
Let's define the different variables we will need. 
In order to search for a user via username and retrieve their tasks, it will be necessary to have a variable to store `tasks` and one to store `usernames`. We also need to store if the tasks for a particular user, once searched, have been loaded to allow a special message for empty task lists (`tasksLoaded`). 

There is also some task-addition specific data to store: the name (`namefortask`) and description (`descfortask`) for a task entered in the form. 

For deleting tasks when a task is clicked, we need a `clickedTaskName` and a variable to store if a request to delete a certain task should be sent to the backend (`sendDeleteRequest`). 

For displaying user error messages, we need `errorForUser`, for retrieving the username of the currently active user sent from logging in/registering we will need to set a "location" variable using `useLocation()`, and in order to redirect to other pages we will need to define a "navigate" variable with `useNavigate()`

Now, define all of these at the top of the `App()` function with useState and their defaults, along with "location" and "navigate": 
```jsx
const location = useLocation();

const [tasks, setTasks] = useState([]); // defaults to an empty list
const [username, setUsername] = useState(location.state?.username || ""); // defaults to the username of the logged-in user or an empty string if not available
const [namefortask, setnamefortask] = useState(""); // defaults to an empty string before the user has typed anything
const [descfortask, setdescfortask] = useState(""); // defaults to an empty string before the user has typed anything
const [tasksLoaded, setTasksLoaded] = useState(false); // defaults to false since tasks are loaded when the user submits a name, and no name has been submitted initially
const [clickedTaskName, setClickedTaskName] = useState(""); // no task has been clicked yet, so sets clicked task name to an empty string
const [sendDeleteRequest, setSendDeleteRequest] = useState(false); // no task has been clicked so no request to delete a task should be sent to the backend by default
const [errorForUser, setErrorForUser] = useState(""); // no error initially

const navigate = useNavigate(); 
```

## Retrieving Tasks


## Adding Tasks


## Deleting Tasks


## Bonus: Logging Out