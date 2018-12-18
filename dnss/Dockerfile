FROM golang:latest

# Downlaod and install dnss
RUN go get -v blitiri.com.ar/go/dnss

#Run dnss
CMD  [ "/go/bin/dnss", "--help" ]

## Command to get dnss proxying incoming DoH traffic is sudo ./dnss -enable_https_to_dns   -https_key=/home/eldridgea/privkey.pem -https_cert=/home/eldridgea/fullchain.pem 