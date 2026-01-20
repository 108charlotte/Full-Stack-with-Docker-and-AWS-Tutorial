# Running Your Application
Everything is almost set up! 

You are already in the repository directory, so when you run `ls`, you should see a `docker-compose.yaml` file. 

You should now see a `docker-compose.yaml` file, along with the familiar `frontend` and `backend` folders you created and several other files. 

Now, build and run the containers with the following command: 

```bash
docker-compose up -d # the d is for detached, which allows you to close your terminal session without stopping the services
```

You can check the status of your container with the following: 
```bash
docker-compose ps
```

Your application is now up! Go to `http://YOUR_EC2_PUBLIC_IP:5173` to see it on the web (replace YOUR_EC2_PUBLIC_IP with the IPv4 address you copied earlier). 