## Scaling exercise application ##

The project https://github.com/docker-hy/material-applications/tree/main/scaling-exercise(opens in a new tab) is a barely working application. Go ahead and clone it for yourself. The project already includes docker-compose.yml so you can start it by running ``docker compose up``.

The application should be accessible through http://localhost:3000(opens in a new tab). However it doesn't work well enough and we've added a load balancer for scaling. Your task is to scale the compute containers so that the button in the application turns green.

This exercise was created with [Sasu Mäkinen](https://github.com/sasumaki)(opens in a new tab)

Submit the used commands for the answer.

## command
```
docker compose up --scale compute=5
```