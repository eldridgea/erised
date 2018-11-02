A project to only see what you want to see.

This will deploy a docker stack of 3(ish) containers. 

cloudflared (or another DoH/DoT proxy)
pihole (or other DNS based adblocker)
OpenVPN (or other VPN)


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