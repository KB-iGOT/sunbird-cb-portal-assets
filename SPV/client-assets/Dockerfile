FROM node:22.6.0

WORKDIR /usr/src/app

COPY . .

# Install required dependencies (Debian Bookworm has active repos)
RUN apt-get update && \
    apt-get install -y zip libjpeg-turbo-progs nasm && \
    rm -rf /var/lib/apt/lists/*

# Install Node dependencies and build
RUN npm install && npm run build

# Package the build output
RUN zip -r dist.zip dist
