# [Backstage](https://backstage.io)

This is your newly scaffolded Backstage App, Good Luck!

Build the docker image inside `.docker` folder

```sh
docker build . -t mycompany/mkdocs:1.3.2
```

To start the app, run:

```sh
yarn install
yarn dev
```

## Start local Kroki server:

Copy file `app-config.local-example.yaml` and rename-it to `app-config.local.yaml`.

```
docker-compose up
```

## Keeping Backstage updated

Link: https://backstage.io/docs/getting-started/keeping-backstage-updated/