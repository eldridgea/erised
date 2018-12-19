FROM golang:latest

# Downlaod and install dnss
RUN go get -v blitiri.com.ar/go/dnss

# Copy in certificates
COPY fullchain.pem /certs/fullchain.pem
COPY privkey.pem /certs/privkey.pem

# Run dnss
CMD  [ "/go/bin/dnss", "-enable_https_to_dns", "-https_key=/certs/privkey.pem", "-https_cert=/certs/fullchain.pem", "-dns_upstream", "172.28.1.4:52"]
