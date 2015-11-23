## Homework 4 - Advanced Docker

* Create 2 digital ocean droplets.
* Install docker and docker compose

### Task 1.

* Copy code in  [Task 1](https://github.com/shakepreman/devops_hw4/tree/master/Task1)
* Build and run the docker container1 first.
```
docker build -t container1 .
docker run -it --name container1 container1
```

* Build and run the docker container2
```
docker build -t container2 .
docker run -it --link container1:container1 --name container2 container2 curl container1:9001
```

### 2. Task 2

* Create 2 Digital Ocean Droplets (Server/Client)
* Copy server code from [here](https://github.com/shakepreman/devops_hw4/tree/master/Task2/Server) onto first droplet.
* Copy client code from [here](https://github.com/shakepreman/devops_hw4/tree/master/Task2/Client) onto second droplet.

* Run the command on first server 
`docker-compose up`
* Run the command on second server
`docker-compose run Client`

### 3. Task3

* Create a Digital Ocean Droplet
* Copy Deply folder from [here](https://github.com/shakepreman/devops_hw4/tree/master/Task3)
* Clone provided app from [here](https://github.com/CSC-DevOps/App)
* Add a post-commit hook for App from here [here](https://github.com/shakepreman/devops_hw4/tree/master/Task3/App_hooks)
* Modify main.js and push changes to the blue branch.
```
git add main.js
git commit -m "Blah"
git push blue master
```
* Visit to http://<ip for the droplet>:8082 to see changes
* Push to green
```
git push green master
```
* Visit to http://<ip for the droplet>:8081 to see changes

### Screencast
