Thie currently deploys the Caddy container using a Caddy install using a Personal License. 
Make sure to change this if you require the commerical license.


To start this run these commands:
`docker-compose build --build-arg ERISEDHOST=YOUR_HOSTNAME ERISEDEMAIL=YOUR_EMAIL`
Replace YOUR_HOSTNAME with your hostname and YOUR_EMAIL with your email.

Then run `docker-compose up`


















A project to only see what you want to see.

This will deploy a docker stack of 3(ish) containers. 

* cloudflared (or another DoH/DoT proxy)
* pihole (or other DNS based adblocker)
* OpenVPN (or other VPN)
* dnss - receives incoming DoH request and passed to upstream DNS server


For prodcucrization maybe use cloudflare bandwidth alliance, and provide VPN Service.

        ---------
        |       |
        |Device |
        | .     |
        ---------
            |
            |
        DNS Query
            |
            |
        ---------
        |       |
        |VPN    |
        | .     |
        ---------
            |
            |
        DNS Query
            |
            |
        ---------
        |       |
        |pihole |
        | .     |
        ---------   
            |
            |
        DNS Query
            |
            |
        --------------
        |             |
        |cloudoflared |
        | .           |
        --------------
