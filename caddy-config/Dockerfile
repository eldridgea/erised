FROM golang:latest

# Install caddy
# This uses the PERSONAL License. Make sur to change this if you need a commercial license - https://caddyserver.com/download
RUN curl https://getcaddy.com | bash -s personal net

# Copy config
#COPY nginx.conf /etc/nginx/nginx.conf

# Run caddy
CMD  [ "caddy" ]
