FROM ubuntu:latest

# shell form
RUN apt-get update && \ 
    apt-get install -y --no-install-recommends \
    curl \
    && rm -rf /var/lib/apt/lists/*

# exec form
ENTRYPOINT ["curl"]

CMD ["--help"]
