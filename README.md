# docker-shared-volumes

Small repo for playing with sharing volumes across multiple containers.

### Steps for getting this going
1. In the `nginx` directory, run `docker build -t react-nginx`
2. In the `reactapp` directory, run `docker build -t react-app`
3. In the root of the project, run `docker-compose up -d`
4. `localhost:8000` should now have host the sample `index.html`
5. ???
6. Profit

### Questions
- Since the react image is just holding static files, it has no process and thus exits immediately
  - if the NGINX container were to bounce, would the `app` volume still hold the react image's static files?
  - what's the lifecycle of the `app` volume in docker-compose? kubernetes?
