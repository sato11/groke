FROM openjdk:8-jdk-alpine
WORKDIR /embulk
RUN apk --update add && \
    apk add curl postgresql-client
RUN curl --create-dirs -o /usr/local/bin/embulk -L "https://dl.embulk.org/embulk-latest.jar" && \
    chmod +x /usr/local/bin/embulk
