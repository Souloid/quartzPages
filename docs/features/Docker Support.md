---
created: 2024-07-07 @ 23:03:09 PM
updated: 2024-07-07 @ 23:03:09 PM
---
Quartz comes shipped with a Docker image that will allow you to preview your Quartz locally without installing Node.

You can run the below one-liner to run Quartz in Docker.

```sh
docker run --rm -itp 8080:8080 $(docker build -q .)
```
