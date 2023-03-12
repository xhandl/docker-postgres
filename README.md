# Postgres
### Run and go Docker setup for PostgreSQL with simple web administration via Adminer.

<br />

To start PostgreSQL on background via Docker just type:
```
docker compose up -d
```

Main parametrs can be modified via `.env` file.


Default configuration:
```
IMAGE: postgres:15.2
CONTAINER NAME: postgres
PORT: 5432
SERVER: localhost
USER: postgres
PASSWORD: admin
```

Data are persisted locally:
```
./volumes/postgresql/data
```

Admined web administration:
```
IMAGE: adminer:4.8.1
CONTAINER NAME: adminer
PORT: 8080
URL: http://localhost:8080
SERVER: postgres
USER: postgres
PASSWORD: admin
```

Docker network:
```
postgres
```