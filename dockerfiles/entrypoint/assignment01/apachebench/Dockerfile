FROM ubuntu:20.04

# ubuntu does not provide a convenient way to clean the cache directly like alpine does with --no-cache
RUN apt-get update && \
    apt-get install apache2-utils -y && \
    apt-get clean && \
    rm -rf /var/lib/apt/lists/*

CMD [ "-n", "10", "-c", "2", "https://www.bretfisher.com/" ]

# adding healthcheck
HEALTHCHECK --interval=30s --timeout=30s --start-period=5s --retries=3 \
    CMD [ "-n", "1", "-c", "1", "https://www.google.com/" ] || exit 1

ENTRYPOINT [ "ab" ]