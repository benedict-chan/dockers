#
# https://github.com/ytdl-org/youtube-dl
#

FROM alpine


RUN set -xe \
    && apk add --no-cache ca-certificates \
                          ffmpeg \
                          openssl \
                          python3 \
                          aria2 \
    && pip3 install youtube-dl



WORKDIR /data

#ENTRYPOINT ["/bin/ash"]
CMD ["/bin/ash"]

