FROM node:lts-fermium as web-app
LABEL maintainer="abyweinberg@gmail.com"
 
#RUN apt update -y
WORKDIR /app

COPY ./package.json /app/package.json
COPY ./package-lock.json /app/package-lock.json

RUN npm install
COPY . .
# The build is commented to increase 
# RUN node_modules/.bin/ng build frontend
EXPOSE 3000
CMD [ "npm", "start" ]
