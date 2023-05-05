#Dockerfile-1
#installing apache2 and copying custom index.html
FROM ubuntu:latest
RUN sudo su -
RUN apt-get update -y
RUN apt-get install -y apache2
RUN service apache2 start
RUN service apache2 status
RUN rm var/www/html/index.html
RUN echo "<h1>My First Heading</h1>" >> /var/www/html/index.html
RUN service apache2 restart
RUN service apache2 status
EXPOSE 80
CMD apachectl -D FOREGROUND
