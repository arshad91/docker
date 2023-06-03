FROM node:13-alpine

ENV MONGO_DB_USERNAME=admin \
    MONGO_DB_PWD=password

#RUN command is used to run any linx command in docker container 
RUN mkdir -p /home/app

#COPY command is used to copy from local laptop to container. we could have used RUN cp command but this would run in container only so willl not be able to copy from laptop
COPY ./app /home/app

# set default dir so that next commands executes in /home/app dir
WORKDIR /home/app

# will execute npm install in /home/app because of WORKDIR
RUN npm install

# CMD is entrypoint command. no need for /home/app/server.js because of WORKDIR
CMD ["node", "server.js"]

