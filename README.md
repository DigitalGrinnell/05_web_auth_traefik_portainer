# 05_web_auth_traefik_portainer
This `isle-docker-compose` project adds a pop-up 'admin' authentication challenge to ISLE's Traefik and Portainer dashboards.

## Overview
This project modifies the Traefik and Portainer dashboard commands providing both services with password protection for the `admin` user.  

## Why Do I Need This?
The Traefik and Portainer dashboards that ISLE spins up from `docker-compose.yml` are meant for use in development ONLY; they do not provide secure, protected interfaces.  

## How Does This Work?
This project introduces a hashed `admin` password for each dashboard and requires the user to authenticate through an interface that looks something like this:

![Image Here]

## The isle-docker-compose Command
See https://github.com/DigitalGrinnell/ISLE_docker_compose for details.

## How Is This Used?
It's easy, assuming the `isle-docker-compose` command is already defined, just follow these steps...

  1) Open a terminal to your ISLE host, and in that terminal...  
  2) Navigate (`cd`) your working directory to ISLE, the directory that holds your `docker-compose.yml` file. Probably `cd /opt/ISLE`.
  3) Navigate (`cd`) into your `ISLE_docker_compose` directory with: `cd ISLE_docker_compose`.
  4) `git clone` this repository to your ISLE host using `git clone https://github.com/DigitalGrinnell/05_web_auth_traefik_portainer.git; cd ..`.  
  5) Spin up your ISLE instance using our special form of `docker-compose up`, like so: `./isle-docker-compose`.
  6) Your ISLE instance should spin up just as if you had issued `docker-compose up -d`, but with this feature engaged.
