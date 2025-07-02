FROM alpine:3.22.0

RUN apk add --no-cache cmatrix=2.0-r2

# the above command is similar to the one below but more efficient
# RUN apk update && \
#   apk add cmatrix=2.0-r2 && \
#    rm -r /var/cache/apk/*

CMD [ "-abs",  "-C",  "red" ]

#? How to provide a default --help argument when no arguments are provided at runtime

ENTRYPOINT [ "cmatrix" ]
