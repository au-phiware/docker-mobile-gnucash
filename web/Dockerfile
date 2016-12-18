FROM nginx:1.10

ENV DEBIAN_FRONTEND noninteractive
RUN apt-get update \
 && apt-get install -y \
    ssl-cert \
 && rm -rf /var/lib/apt/lists/*
