FROM nginx

RUN apt-get update -y \
    && apt-get install -y apache2-utils \
    && rm -rf /var/lib/apt/lists/*

ENV PROXY_HOST=localhost
ENV PROXY_PORT=80

WORKDIR /opt

COPY auth.conf auth.htpasswd launch.sh ./

RUN chmod 0755 ./launch.sh

CMD ["./launch.sh"]