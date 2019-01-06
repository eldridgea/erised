FROM golang:latest

ARG ERISEDHOST
ARG ERISEDEMAIL

# Install caddy
# This uses the PERSONAL License. Make sure to change this if you need a commercial license - https://caddyserver.com/download
RUN curl https://getcaddy.com | bash -s personal net

# Copy configs
COPY net.conf  /root/net.conf

# Update config file with build variables
RUN sed -i "s/FQDN_NAME_HERE/$ERISEDHOST/" /root/net.conf 
RUN sed -i "s/EMAIL_ADDRESS_HERE/$ERISEDEMAIL/" /root/net.conf

# Set CADDYPATH variable to point where certificates will be stored
ENV CADDYPATH=/root/.caddy

# Run caddy
CMD  [ "caddy", "-type=net", "-agree", "-conf", "/root/net.conf" ]
