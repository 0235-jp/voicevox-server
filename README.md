# voicevox-server

## Usage
Set various parameters in .env.
```
$ cp env.example .env
$ vim .env
```

Create password
```
$ echo $(htpasswd -nb username password) | sed -e s/\\$/\\$\\$/g
```

Create network
```
$ docker network create web
```

If you start up with docker compose
```
$ docker compose up -d
```

If you want to stop the server, you can use the following command.
```
$ docker compose down
```

If you want to use a domain, set API_HOST in .env and start up traefik.
```
$ docker compose -f traefik.yml up -d
```

If you want to stop traefik, you can use the following command.
```
$ docker compose -f traefik.yml down
```
