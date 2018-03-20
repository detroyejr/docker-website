## NGINX Base.
FROM nginx:1.13

## Image information.
LABEL MAINTAINER="Jonathan De Troye"
LABEL EMAIL="detroyejr@outlook.com"

## Add any packages that need to be installed.
RUN apt-get update && \
    apt-get install git -y

## A directory for NGINX is created. The static website is stored on github
## where it can be cloned. The 'public' directory creaed by blogdown
## is copied into here.
RUN mkdir /www && \
    chown nginx:nginx /www

COPY nginx.conf /etc/nginx/nginx.conf

## Clone website and move the public directory to www/public.
RUN git clone https://github.com/detroyejr/website /website
RUN cp -r website/public /www/public
