FROM nginx:1.9.12

MAINTAINER NGINX Docker Maintainers "docker-maint@nginx.com"

RUN apt-get update && \
	apt-get install -y ca-certificates gettext-base && \
	rm -rf /var/lib/apt/lists/* && \
    rm /etc/nginx/conf.d/*

EXPOSE 80 443

COPY nginx-ingress /
COPY nginx/ingress.tmpl /

CMD ["/nginx-ingress"]
