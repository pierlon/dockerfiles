FROM node:alpine

LABEL maintainer=pierregordon@protonmail.com

RUN apk update && \
    apk add --no-cache git && \
    cd /opt && \
    git clone https://github.com/lockfale/OSINT-Framework.git && \
    cd OSINT-Framework && \
    yarn install && \
    yarn global add http-server

EXPOSE 8080

WORKDIR /opt/OSINT-Framework

CMD cd public && http-server
