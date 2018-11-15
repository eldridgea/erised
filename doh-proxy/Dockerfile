FROM alpine:latest

#Install Python3 & DoH-proxy
RUN apk add python3
RUN pip3 install --upgrade pip
RUN pip3 install doh-proxy

#Run doh-proxy
CMD  [ "doh-proxy", "--listen-address=0.0.0.0", "--upstream-resolver=1.1.1.1", "--certfile=/certs/fullchain.pem", "--keyfile=/certs/privkey.pem" ]