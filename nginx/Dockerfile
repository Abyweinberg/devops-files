FROM nginx

RUN apt update
RUN apt install vim certbot python3-certbot-nginx -y

COPY ./*.conf /etc/nginx/conf.d/

EXPOSE 80 443

#ENTRYPOINT ["nginx", "-g", "daemon off;"]
