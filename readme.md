# Welcome to the Anythink Market repo

To start the app use Docker. It will start both frontend and backend, including all the relevant dependencies, and the db.

Please find more info about each part in the relevant Readme file ([frontend](frontend/readme.md) and [backend](backend/README.md)).

## Development

When implementing a new feature or fixing a bug, please create a new pull request against `main` from a feature/bug branch and add `@vanessa-cooper` as reviewer.

## First setup

### Docker setup

So first thing’s first - [install Docker](https://docs.docker.com/get-docker/).

Test your docker installation by running the following commands on your terminal:

```
docker -v
docker-composer -v
```

### Run the application

Run docker-compose

```
docker-compose up
```

### Run the DB migrations

```
docker exec -ti  -w /usr/src/backend anythink-backend bin/rails db:migrate
```

### Test the installation

Open http://localhost:3000/api/ping in your broswer to test the backend and http://localhost:3001 to test the frontend. If everything is working properly, you’ll be able to create a new user on http://localhost:3001/register
