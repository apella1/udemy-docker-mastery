FROM drupal:11.2.2

RUN apt-get update \
    && apt-get install -y git \
    && apt-get clean \
    && rm -rf /var/lib/apt/lists/*

WORKDIR /var/www/html/themes

RUN git clone --branch 8.x-4.x --single-branch --depth 1 https://git.drupalcode.org/project/bootstrap.git \
    && chown -R www-data:www-data bootstrap

WORKDIR /var/www/html
