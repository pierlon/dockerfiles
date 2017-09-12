FROM alpine

LABEL maintainer=pierregordon@protonmail.com

ENV GIT_FTP_VERSION 1.4.0

RUN apk add --no-cache \
        git \
        curl \
        bash \
    && apk add --no-cache --virtual .build-deps \
        tar \
    && curl -SLO "https://github.com/git-ftp/git-ftp/archive/$GIT_FTP_VERSION.tar.gz" \
    && tar -xf "$GIT_FTP_VERSION.tar.gz" \
    && mv git-ftp-$GIT_FTP_VERSION/git-ftp /usr/local/bin/ \
    && rm -rf $GIT_FTP_VERSION.tar.gz git-ftp-$GIT_FTP_VERSION \
    && apk del .build-deps
