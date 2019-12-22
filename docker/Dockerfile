FROM debian:9

WORKDIR /app
COPY . app.py /app/

RUN apt-get update -yq \
&& apt-get install nginx -yq \
&& sudo ufw allow 'Nginx HTTP'

EXPOSE 80

CMD systemctl start nginx
