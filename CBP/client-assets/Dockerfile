FROM node:16

RUN sed -i 's|http://deb.debian.org/debian|http://archive.debian.org/debian|g' /etc/apt/sources.list && \
    sed -i 's|http://security.debian.org/debian-security|http://archive.debian.org/debian-security|g' /etc/apt/sources.list && \
    echo 'Acquire::Check-Valid-Until "false";' > /etc/apt/apt.conf.d/99no-check-valid-until && \
    apt update && \
    apt install -y zip libjpeg-turbo-progs nasm

RUN useradd -ms /bin/bash node && \
    mkdir -p /usr/src/app && \
    chown -R node:node /usr/src/app

WORKDIR /usr/src/app

COPY --chown=node:node . .

USER node
    
RUN npm install && npm run build

RUN zip -r dist.zip dist
