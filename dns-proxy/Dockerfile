FROM golang:latest

#Install cloudflared
RUN go get github.com/cloudflare/cloudflared/cmd/cloudflared

CMD [ "cloudflared", "proxy-dns", "--address", "0.0.0.0" ]
