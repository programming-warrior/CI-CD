FROM node:20.12.0-alpine3.19
WORKDIR /usr/src
COPY . .
RUN  NODE_ENV=development npm install
RUN npm run db:migrate
RUN npm run build
cmd ["npm","run","start-user-app"]



#not the right way since package.json file of all the subdirectory inside the apps wil be copied to the usr/src/apps-> thus, it will have more than one package.json

#copy each sub directory package.json seperately

# WORKDIR /usr/src/apps

# copy ./apps/**/package.json ./apps/**/package-lock.json ./

# run "npm install"

# WORKDIR /usr/src/packages

# copy ./packages/**/package.json ./packages/**/package-lock.json ./

# run "npm install"

# WORKDIR /usr/src


