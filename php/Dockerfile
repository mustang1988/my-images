FROM mustang1988/my-images:nginx

WORKDIR /etc/

COPY supervisord.conf

ENTRYPOINT ["supervisord","-c","/etc/supervisord.conf"]