FROM debian:10

# Установка необходимых пакетов
RUN apt-get update && \
    apt-get install -y apt-transport-https ca-certificates curl gnupg lsb-release

# Установка Docker
RUN curl -fsSL https://download.docker.com/linux/debian/gpg | gpg --dearmor -o /usr/share/keyrings/docker-archive-keyring.gpg && \
    echo "deb [arch=amd64 signed-by=/usr/share/keyrings/docker-archive-keyring.gpg] https://download.docker.com/linux/debian $(lsb_release -cs) stable" | tee /etc/apt/sources.list.d/docker.list > /dev/null && \
    apt-get update && \
    apt-get install -y docker-ce docker-ce-cli containerd.io 

# Копирование Docker репозитория
COPY ./repo /app/repo

## Установка docker-compose
#RUN curl -sSL https://github.com/docker/compose/releases/download/1.29.2/docker-compose-Linux-x86_64 -o /usr/local/bin/docker-compose && \
#    chmod +x /usr/local/bin/docker-compose
#
## Запуск контейнеров из docker-compose.yml
#WORKDIR /app/repo
#CMD ["docker-compose", "up"]
