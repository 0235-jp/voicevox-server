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
$ docker compose up -d --scale voicevox-api=xx
```

If you want to stop the server, you can use the following command.
```
$ docker compose down
```
