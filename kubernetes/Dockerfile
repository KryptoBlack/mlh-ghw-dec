FROM node:18-alpine@sha256:67373bd5d90ea600cb5f0fa58d7a5a4e6ebf50b6e05c50c1d1cc22df5134db43

LABEL MAINTAINER="KryptoBlack"

# copy package.json to /usr/src dir in the container
RUN mkdir /usr/src
COPY package.json /usr/src
WORKDIR /usr/src

# install dependencies
RUN yarn install

# copy rest of the source code to container
COPY . .

EXPOSE 8080

ENTRYPOINT [ "yarn", "start" ]