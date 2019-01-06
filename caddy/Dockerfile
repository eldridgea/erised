FROM golang:latest

# Install caddy
# This uses the PERSONAL License. Make sure to change this if you need a commercial license - https://caddyserver.com/download
RUN curl https://getcaddy.com | bash -s personal net

# Copy configs
COPY net.conf  /root/net.conf


# Set CADDYPATH variable to point where certificates will be stored
ENV CADDYPATH=/root/.caddy

# Run caddy
CMD  [ "caddy", "-type=net", "-agree", "-email", "eldridgea@gmail.com", "-conf", "/root/net.conf" ]
