# using nodejs version 18
FROM node:18
#EXPOSE functions as a type of documentation between the person who builds the image and the person who runs the container
EXPOSE 8080
# chaning current diretory to /opt/server
WORKDIR /opt/server
ENV MONGO=true
# copying package.json to /opt/server location
COPY package.json /opt/server
# copying server.js to /opt/server location
COPY server.js /opt/server
# installing dependencies
RUN npm install
# keeping node and server.js active forever
CMD ["node", "server.js"]

# No need to give mongodb URL in catalogue since server.js (line 135) contains name "monogobd" with which catalogue will connect and load into to monodb databse 

# docker build -t catalogue:v1 . <---to build image

# docker run -d --name catalogue --network=roboshop catalogue:v1 <--- to create and run container with name, in roboshop network

# docker ps <-- to see running container
# docker logs catalogue <-- to see logs of catalogue