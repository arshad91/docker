## demo app - developing with Docker

This demo app shows a simple user profile app set up using 
- index.html with pure js and css styles
- nodejs backend with express mode
- mongodb for data storage

All components are docker-based

#### To start the application

Step 1: start mongodb and mongo-express
_You can access the mongo-express under localhost:8080 from your browser_

http://0.0.0.0:8081/

Step 2: in mongo-express UI - create a new database "user-account"

Step 3: in mongo-express UI - create a new collection "users" in the database "user-account"       
    
Step 4: start node server 

    node server.js
    
_You can access the application under localhost:3000 from your browser_

#### To build a docker image from the application

    docker build -t my-app:1.0 .       
    
The dot "." at the end of the command denotes location of the Dockerfile.

#docker compose takes care of creating common network
