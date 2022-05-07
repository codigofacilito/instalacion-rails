Dockerfile

```bash

FROM ruby:3

RUN apt-get update && apt-get install \
    nodejs \
    curl \
    sqlite3 \
    yarn -y

RUN gem install bundler

RUN gem install rails

```

Configuración Docker compose (docker-compose.yml)

```bash

version: '3'

services:
  rails:
    build: .
    tty: true
    ports:
      - 3000:3000
    volumes:
      - .:/app

```

Para ejecutar el servidor recuerda hacerlo de esta manera

```bash
rails s -b 0.0.0.0
```