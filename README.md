ELK stack from scratch, with Docker
===================================

## Run (stack)
```
  # run (daemon)
  docker-compose up -d
  # show logs
  docker-compose logs -f
```

## Run the webapp to monitor
```
  docker build ./webapp -t dockerelkstack_webapp
  docker run --network dockerelkstack_logging --link redis:redis -p 80:80 -d --name webapp dockerelkstack_webapp
```
Then navigate on the site (port 80, source: https://github.com/sbilly/joli-admin)