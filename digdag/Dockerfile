FROM openjdk:8-jdk-alpine
WORKDIR /digdag
RUN apk --update add && \
    apk add curl postgresql-client
RUN curl --create-dirs -o /usr/local/bin/digdag -L "https://dl.digdag.io/digdag-latest" && \
    chmod +x /usr/local/bin/digdag
COPY ./server.properties /digdag/server.properties
EXPOSE 65432
CMD digdag server -c server.properties -A log/accesslogs -O log/tasklogs -L log/server.log
