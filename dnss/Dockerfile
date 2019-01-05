FROM golang:latest

# Downlaod and install dnss
RUN go get -v blitiri.com.ar/go/dnss
RUN mkdir /certs

# Generates self signed certs to encrypt traffic between here and Caddy
RUN openssl req  -nodes -new -x509  -keyout /certs/server.key -out /certs/server.cert -batch 

# Run dnss
CMD  [ "/go/bin/dnss", "-enable_https_to_dns", "-https_key=/certs/server.key", "-https_cert=/certs/server.cert", "-dns_upstream", "172.28.1.4:53"]
