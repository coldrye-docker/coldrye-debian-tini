FROM coldrye/debian:testing-latest

MAINTAINER Carsten Klein <trancesilken@gmail.com>

ARG TINI_VERSION="v0.9.0"

RUN set -x \
    && export TINI_HOME="/usr/local/sbin" \
    && curl -fSL "https://github.com/krallin/tini/releases/download/$TINI_VERSION/tini" -o "${TINI_HOME}/tini" \
    && curl -fSL "https://github.com/krallin/tini/releases/download/$TINI_VERSION/tini.asc" -o "${TINI_HOME}/tini.asc" \
    && export GNUPGHOME="$(mktemp -d)" \
    && gpg --keyserver ha.pool.sks-keyservers.net --recv-keys 6380DC428747F6C393FEACA59A84159D7001A4E5 \
    && gpg --batch --verify "${TINI_HOME}/tini.asc" "${TINI_HOME}/tini" \
    && rm -r "$GNUPGHOME" "${TINI_HOME}/tini.asc" \
    && chmod +x "${TINI_HOME}/tini" \
    && "${TINI_HOME}/tini" -h

