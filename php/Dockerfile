FROM mustang1988/my-images:nginx

WORKDIR /etc/

RUN rm -rf /etc/supervisord.conf

COPY supervisord.conf /etc/supervisord.conf

COPY start.sh /start.sh

EXPOSE 9001

ENTRYPOINT ["sh","/start.sh"]