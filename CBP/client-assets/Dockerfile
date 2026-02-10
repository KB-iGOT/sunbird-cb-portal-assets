FROM node:16

RUN sed -i 's|http://deb.debian.org/debian|http://archive.debian.org/debian|g' /etc/apt/sources.list && \
    sed -i 's|http://security.debian.org/debian-security|http://archive.debian.org/debian-security|g' /etc/apt/sources.list && \
    echo 'Acquire::Check-Valid-Until "false";' > /etc/apt/apt.conf.d/99no-check-valid-until && \
    apt-get update && \
    apt-get install -y --no-install-recommends zip libjpeg-turbo-progs nasm && \
    rm -rf /var/lib/apt/lists/*

RUN useradd -ms /bin/bash appuser && \
    mkdir -p /usr/src/app && \
    chown -R appuser:appuser /usr/src/app

WORKDIR /usr/src/app

USER appuser

RUN npm ci

COPY --chown=appuser:appuser . .
    
RUN npm install && npm run build

RUN zip -r dist.zip dist
