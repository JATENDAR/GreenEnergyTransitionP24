# Project2024

## Getting started

To install all dependencies we need to run the install in Docker container.
So instead of `npm install` we need to run `npm run setup`

## Start the app in development mode (all in docker)

In .env file set POSTGRES_HOST to db

First
`npm run setup`
then
`docker compose up`

Open http://localhost:8000

## Start the app in development mode (just db in docker)

In .env file set POSTGRES_HOST to localhost

First
`npm install`
then
`docker-compose up db`
finally
`npm run startbe`
and
`npm run startfe`

Open http://localhost:4200

## Start the app in production mode

In .env file set POSTGRES_HOST to db

First
`npm run build`
then
`docker-compose -f docker-compose.production.yml build`
and finally
`docker-compose -f docker-compose.production.yml up`

Open http://localhost:80 (port is optional)
