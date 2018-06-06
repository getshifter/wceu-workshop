# Docker Compose: Hello World

A simple example of a single container using Docker Compose.

```
version: '3.3'

services:
 
  hello-world:
    image: nginx
    ports:
      - "8000:80"
```