# spinup

A collection of scripts to help spin up Ubuntu/Debian Virtual Machines.

These scripts are to be run on *FRESH INSTALLS ONLY*.

I test these on $5/mo SSD cloud servers from Digital Ocean! Please use my
referral code if you would like to give them a try. It helps me keep the
lights on :-)

https://www.digitalocean.com/?refcode=a0f6a3bca1c8

# License: MIT

Copyright (c) 2013 Jared De Blander

Permission is hereby granted, free of charge, to any person obtaining a copy of
this software and associated documentation files (the "Software"), to deal in
the Software without restriction, including without limitation the rights to
use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of
the Software, and to permit persons to whom the Software is furnished to do so,
subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS
FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR
COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER
IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN
CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.

# Package Notes

## Gunicorn Worker

Hookup your WSGI Python Apps and prepare them for webs server of choice. Web
server not included (unless you count Gunicorn).

## NGINX Web Server

Ready to cluster Gunicorn workers? This is still W.I.P. I have a config file
where I left off included in this repo. See: nginxpy.conf

## MariaDB Galera Cluster

Heavily incomplete. Intended to spin up a MariaDB galera cluster VM.

## CouchDB

## CHC: HHVM + CouchDB +  Composer
Want the bleeding edge? It doesn't get easier than this. Package Management,
Facebook's HHVM JiT & one of the simplest NoSQL Databases with point and click
replication. Currently uses Ubuntu 13.10

### Ports
* 22: SSH
* 80: HTTP
* 5984: CouchDB

# ToDo

1. Split Python into a Gunicon workers spinup and an NGINX reverse proxy spinup.
2. Create a MariaDB spinup.
3. Create a MongoDB spinup.

# Instructions

Run these commands as the root user.

## Solo Apps

### Gunicorn Worker

    bash <(wget -qO- https://raw.github.com/jared0x90/spinup/master/spin-gunicorn.sh)

### NGINX Web Server

    bash <(wget -qO- https://raw.github.com/jared0x90/spinup/master/spin-nginx.sh)

### Deluge Thin Client

    bash <(wget -qO- https://raw.github.com/jared0x90/spinup/master/spin-deluge.sh)

### MariaDB Galera Cluster

    bash <(wget -qO- https://raw.github.com/jared0x90/spinup/master/spin-galera.sh)

### CouchDB

    bash <(wget -qO- https://raw.github.com/jared0x90/spinup/master/spin-couch.sh)
## Stacks

### CHC: CouchDB + HHVM + Composer

    bash <(wget -qO- https://raw.github.com/jared0x90/spinup/master/spin-couchdb-hhvm+composer.sh)
