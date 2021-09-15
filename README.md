# Sentry

# First Setup

- Up Redis

```docker-compose up -d redis```

- Up Postgres

```docker-compose up -d postgres```

- Generate Secret

```docker-compose run sentry config generate-secret-key```

The SENTRY_SECRET_KEY will show something like this:

```5ghn&ms(pwb+=_mnur+)(1v2sg0@hx-#a^rmhij)n5dnqwpg4d```

You need to keep it! So, with SENTRY_SECRET_KEY in hands, you need to put in on .env file (just on SENTRY_SECRET_KEY parameter) and run the following command:

```docker-compose run sentry upgrade```

## Running Sentry

```docker-compose up -d sentry cron worker```