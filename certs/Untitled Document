#!/bin/bash

openssl req -x509 -nodes -days 365 -newkey rsa:2048 \
    -keyout certs/private/website.key \
    -out certs/certs/website.crt \
    -subj "/C=US/ST=Massachusetts/L=Boston/O=DavidUpton/OU=Home/CN=$SITE_NAME"
