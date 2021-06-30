FROM node:lts-fermium as web-app
LABEL maintainer="abyweinberg@gmail.com"
 
#RUN apt update -y
WORKDIR /app

COPY ./package.json /app/package.json
COPY ./package-lock.json /app/package-lock.json

RUN npm install
COPY . .

EXPOSE 3007
CMD ["node", "app.js"]


# FROM node:10 AS ui-build
# WORKDIR /usr/src/app
# COPY my-app/ ./my-app/
# RUN cd my-app && npm install @angular/cli && npm install && npm run build
# 
# FROM node:10 AS server-build
# WORKDIR /root/
# COPY --from=ui-build /usr/src/app/my-app/dist ./my-app/dist
# COPY package*.json ./
# RUN npm install
# COPY server.js .
# 
# EXPOSE 3080
# 
# CMD ["node", "server.js"]
# 
# 
# FROM node:lts
# LABEL maintainer="abyweinberg@gmail.com"
# 
# RUN apt update -y
# RUN apt install vim -y
# # I need snapd to install certboot but snapd need systemd to been in the system (boot)
# RUN apt install snapd -y
# I have to create ln -s /usr/lib/snapd/snapd and run it 
# RUN npm i express -g

# RUN npx express-generator --view=pug stam.com
# WORKDIR /var/www/html/stam.com
# RUN npm install

# RUN npx express-generator --view=pug something.com
# WORKDIR /var/www/html/something.com
# RUN npm install
# WORKDIR /root/hello-world
# RUN npm i


