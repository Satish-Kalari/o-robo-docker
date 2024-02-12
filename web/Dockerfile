FROM nginx
# removing index.html from /usr/share/nginx/html/ location
RUN rm -rf /usr/share/nginx/html/index.html
# copying local roboshop.conf file to /etc/nginx/default.d/roboshop.conf location
COPY roboshop.conf /etc/nginx/default.d/roboshop.conf
# COPY and ADD are same, ADD has two extra function, copying from URL and untar
# assing static folde from local to /usr/share/nginx/html/ location
ADD static /usr/share/nginx/html/

# docker build -t web:v1 <---to build image

# docker run -d -p 80:80 --name web --network=roboshop catalogue:v1 <--- to create and run container with name, in roboshop network with 80 prot

# docker ps <-- to see running container
# docker logs web <-- to see logs of web