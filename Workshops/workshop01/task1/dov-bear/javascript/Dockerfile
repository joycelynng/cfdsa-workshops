FROM node:21

# create the /app directory, cd into /app
WORKDIR /app

# How to build the application
# inside /app
# copy files from local into the container
COPY main.js .
COPY package-lock.json .
COPY package.json .

COPY public public
COPY views views

# Install dependencies
RUN npm ci

# How to run the application

# Environment variables
ENV PORT=5000
ENV INSTANCE_NAME='name'
ENV INSTANCE_HASH='hash'

# Tell the container what port the application need
EXPOSE ${PORT}

ENTRYPOINT node main.js