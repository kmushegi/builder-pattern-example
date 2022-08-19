# Docker Build Interview Exercise

1. Checkout the `challenge` branch of the repository like below
```
git clone -b challenge --single-branch git@github.com:kmushegi/builder-pattern-example.git
```

The goal of this challenge is to produce a Docker image that serves static assets of a React app using nginx.

## React
React app base image: `node:12.13.0-alpine`

Copy repository contents to `/app` directory in the image

Build steps:
* install dependencies: `npm install`
* build artifacts: `npm run build`, artifacts created in `./build` directory

## NGINX

NGINX base image: `nginx:latest`

NGINX Config: `./nginx/default.conf`, in the image must be in `/etc/nginx/conf.d/default.conf`

Artifacts destination in the image: `/usr/share/nginx/html`

Expose app on port `3000`
