FROM        --platform=$TARGETOS/$TARGETARCH python:3.13-alpine

LABEL       author="Kevin Patino" maintainer="kevin@kevinpatino.com"

RUN         apk add --update --no-cache bash cmake make ca-certificates curl ffmpeg g++ gcc git openssl sqlite tar tzdata \
            && adduser -D -h /home/container container

USER        container
ENV         USER=container HOME=/home/container
WORKDIR     /home/container

COPY        ./../entrypoint.sh /entrypoint.sh
CMD         [ "/bin/bash", "/entrypoint.sh" ]