FROM php:latest

RUN apt-get update && apt-get install -y git && rm -rf /var/lib/apt/lists/*

RUN git clone https://github.com/juzeon/fast-mail-bomber.git /fast-mail-bomber && cp /fast-mail-bomber/config.example.php /fast-mail-bomber/config.php

WORKDIR /fast-mail-bomber

ENTRYPOINT ["php", "/fast-mail-bomber/index.php", "start-bombing"]
