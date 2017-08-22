# Faye docker container

Docker image with Ruby and Faye.

Docker image 1.2.4 using Faye 1.2.4, based on [ruby:2.3.4-alpine3.4](https://hub.docker.com/_/ruby/).

## Example Usage

```
version: '2.1'

services:
  faye:
    image: setanta/faye:1.2.4-alpine
    working_dir: /app
    volumes:
      - .:/app:ro
    ports:
      - 9292:9292
    command: rackup config.ru -s thin -p 9292 -E production
```

**Docker Hub:** [setanta/faye](https://hub.docker.com/r/setanta/faye/)
