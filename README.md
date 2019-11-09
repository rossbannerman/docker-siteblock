# docker-siteblock

## About
A simple container based siteblocker.  

## Docker Hub
The following images are used:
- [rossbannerman/dnsmasq](https://hub.docker.com/r/rossbannerman/dnsmasq/)
- [nginx:alpine-stable](https://hub.docker.com/_/nginx/)

## Usage
1. Add your upstream nameservers of choice to `${PWD}/conf/resolv.conf` (eg. 1.1.1.1, 8.8.8.8)
2. Add the domains you wish to block to `${PWD}/conf/dnsmasq/siteblock.conf`
3. Optional: Edit `${PWD}/conf/nginx/index.html` to edit or replace the page served when a domain is blocked
4. Run `docker-compose up -d`
5. Point the DNS config of your host(s) to the IP of your docker host (and/or localhost if using locally)
