# Helpful Docker Snippets
We are using docker-compose to run locally, but these are helpful Dockerfile examples.

- Build local image from dockerfile: `docker build . --tag gcr.io/strict-chef/cloud-run-node-example`
- Run local image from dockerfile: `PORT=8080 && docker run -it --mount 'type=bind,source=/Users/matt/repos/cloudrun-concepts/cloud-run-node-example,target=/usr/src/app' -p 9090:${PORT} -e PORT=${PORT} gcr.io/strict-chef/cloud-run-node-example`

