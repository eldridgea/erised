FROM debian:latest

# Install nginx
RUN apt-get update
RUN apt-get -y install nginx

# Copy config
COPY nginx.conf /etc/nginx/nginx.conf

# Run nginx
CMD  [ "nginx" ]
