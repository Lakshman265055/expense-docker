FROM nginx:mainline-alpine3.20-slim
RUN rm -rf /etc/nginx/nginx.conf && \
    rm -rf /etc/nginx/conf.d/default.conf && \
    mkdir -P /var/cache/nginx/client_temp && \
    mkdir -P /var/cache/nginx/proxy_temp && \
    mkdir -P /var/cache/nginx/fastcgi_temp && \
    mkdir -P /var/cache/nginx/uwsgi_temp && \
    mkdir -P /var/cache/nginx/scgi_temp && \
    chown -R nginx:nginx /var/cache/nginx && \
    chwon -R nginx:nginx /etc/nginx/ && \
    chmod -R 755 /etc/nginx/ && \
    chown -R nginx:nginx /var/log/nginx && \
    touch /var/run/nginx.pid && \
    chown -R nginx:nginx /var/run/nginx.pid /run/nginx.pid
COPY nginx.conf /etc/nginx/nginx.conf
COPY code /usr/share/nginx/html
USER nginx