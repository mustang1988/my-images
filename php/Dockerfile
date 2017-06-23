FROM mustang1988/my-images:nginx

WORKDIR /etc/

RUN rm -rf /etc/supervisord.conf

COPY supervisord.conf /etc/supervisord.conf

COPY start.sh /start.sh

ENTRYPOINT ["sh","/start.sh"]