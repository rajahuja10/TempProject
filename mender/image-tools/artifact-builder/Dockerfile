FROM ubuntu:20.04

ARG MENDER_ARTIFACT_VERSION='3.3.0'

RUN apt-get update && apt-get install -y \
    wget \
    qemu-user-static

RUN wget -q -O /usr/bin/mender-artifact https://d1b0l86ne08fsf.cloudfront.net/mender-artifact/$MENDER_ARTIFACT_VERSION/linux/mender-artifact && chmod +x /usr/bin/mender-artifact

COPY docker-entrypoint.sh /usr/local/bin/
ENTRYPOINT ["/usr/local/bin/docker-entrypoint.sh"]
