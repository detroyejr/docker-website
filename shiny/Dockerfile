## Shiny Server Base.
FROM rocker/shiny:latest

## Image Info.
LABEL MAINTAINER="Jonathan De Troye"
LABEL EMAIL="detroyejr@outlook.com"

## Get git.
RUN apt-get update && \
    apt-get install git -y

RUN rm -r /srv/shiny-server/
## Shiny apps are stored on github. Remove all the test apps and add others into
## that same directory.
USER shiny
