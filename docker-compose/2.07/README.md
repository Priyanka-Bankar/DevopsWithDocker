# Exercise
# 2.7. Bind mount (mandatory exercise)
## Instructions
Postgres image uses a volume by default. Define manually a volume for the database in a convenient location such as in ``./database`` so you should use now a [bind mount]((https://docs.docker.com/engine/storage/bind-mounts/))(opens in a new tab). The image [documentation](https://github.com/docker-library/docs/blob/master/postgres/README.md#where-to-store-data)(opens in a new tab) may help you with the task.

After you have configured the bind mount volume:

- Save a few messages through the frontend
- Run ``docker compose down``
- Run ``docker compose up`` and see that the messages are available after refreshing browser
- Run ``docker compose down`` and delete the volume folder manually
- Run ``docker compose up`` and the data should be gone

```
TIP: To save you the trouble of testing all of those steps, just look into the folder before trying the steps. If it's empty after ``docker compose up`` then something is wrong.

```

Submit the docker-compose.yml as answer.

## commands

```
docker compose up
docker compose down
docker compose up
docker compose down 
sudo rm -rf ./database
docker compose up
```