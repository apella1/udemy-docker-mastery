FROM ubuntu:20.04

# ubuntu does not provide a convenient way to clean the cache directly like alpine does with --no-cache
RUN apt-get update && \
    apt-get install apache2-utils -y && \
    apt-get clean && \
    rm -rf /var/lib/apt/lists/*

ENTRYPOINT [ "ab" ]

CMD [ "--help" ]
