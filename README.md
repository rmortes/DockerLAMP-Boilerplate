# DockerLAMP Boilerplate

> Based on https://github.com/mattrayner/docker-lamp

A quick 'n easy way to spin up a Github-synced LAMP server

## Requisites

### Server

The server needs to be running the [Nginx Reverse Proxy](https://github.com/nginx-proxy/nginx-proxy) Docker image. Additionally the server could be running the [Nginx Proxy's Letsencrypt Companion](https://github.com/nginx-proxy/docker-letsencrypt-nginx-proxy-companion) Docker image.

I personally recommend this [Way to install the proxy](https://github.com/evertramos/docker-compose-letsencrypt-nginx-proxy-companion) as it's the only one that has worked out-of-the-box for me

### Project

In your project there needs to be a file called `.env` with the following variables:

> VIRTUAL_HOST={{ the host you'll be accessing the webpage from }}
>
> LETSENCRYPT_EMAIL={{ the email of the webpage's admin }}

The webpage port defaults to `:80`. To change it, you'll need to tweak `docker-compose.yml`

## Installation

Assuming your repository is a fork of this one, with your project in `./app/`

1. SSH into your server

2. Clone your project in your desired location

3. Start the container (docker-compose up)

4. Wait until lamp says the MySQL database has been created and it's all ready!