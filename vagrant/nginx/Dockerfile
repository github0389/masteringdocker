FROM alpine:latest
LABEL maintener="Isabelle@me.com"
LABEL description="dockerfile installs NGINX"
RUN apk add --update nginx && \
    rm -rf /var/cache/apk/* && \
    mkdir -p /tmp/nginx/
COPY files/default.conf /etc/nginx/conf.d/default.conf
COPY files/nginx.conf /etc/nginx/nginx.conf
ADD  files/html.tar.gz /usr/share/nginx/
EXPOSE 80/tcp
ENTRYPOINT ["nginx"] 
CMD ["-g", "daemon off;"]
