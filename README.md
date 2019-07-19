# Synchronicity marketplace

## Requirements

- An IDM setup and running
- docker & docker-compose installed

## Setup

1.  Clone this repo

2.  Create a network for the marketplace:

    docker network create --gateway 172.29.20.1 --subnet 172.29.20.0/24 synchronicity

3.  Create an `.env` file at the repo root folder:

    # Oauth info from the IDM
    OAUTH2_CLIENT_ID=xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
    OAUTH2_CLIENT_SECRET=xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
    # Paypal account (if needed)
    PAYPAL_CLIENT_ID=xxx
    PAYPAL_CLIENT_SECRET=yyy

4.  (Optional) Change the mysql password in `docker-compose.yml` and `rss-conf/database.properties`

5.  (Optional) Replace `idm.docker` by the host/ip of the IDM if running on a different network

6.  `docker-compose up`
