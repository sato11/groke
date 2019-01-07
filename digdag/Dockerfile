FROM openjdk:8-jdk-alpine
WORKDIR /digdag
RUN apk --update add && \
    apk add curl postgresql-client docker
RUN curl --create-dirs -o /usr/local/bin/digdag -L "https://dl.digdag.io/digdag-latest" && \
    chmod +x /usr/local/bin/digdag
COPY . /digdag
EXPOSE 65432
ENTRYPOINT [ "java", "-jar", "/usr/local/bin/digdag" ]
CMD [ "server", "-c", "server.properties", "-A", "/digdag/log/accesslogs", "-O", "/digdag/log/tasklogs", "-L", "/digdag/log/server.log" ]
