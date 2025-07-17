# Dockerizing Node.js Sample App with Nginx Proxy

This is a simple project about how to dockerize a Node JS app using nginx as a reverse proxy.

# Description

- Used the app [node-js-sample](https://github.com/heroku/node-js-sample).
- Created a Dockerfile to build the app image.
- Utilized Docker Compose to run two services: the node app and the nginx reverse proxy.
- Customized the nginx configuration.

# How it works

- The app container runs on port 5000.
- Nginx acts as a reverse proxy on port 80, redirecting HTTP traffic to the app.
- Volumes mount the custom nginx configuration into the container
- Only port 80 is exposed outside, not the 5000 directly
- Internal Communication between containers is handled via Docker Compose networking.
