FROM alpine
RUN apk add --no-cache curl wget busybox-extras netcat-openbsd python3 py3-pip bash && \
    pip3 install --no-cache-dir awscli && \
    apk del py3-pip
CMD tail -f /dev/null
