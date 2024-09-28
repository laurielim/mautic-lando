# Mautic recommended-project with Lando
Mautic 5.1.1 setup with the Mautic [recommended-project](https://github.com/mautic/recommended-project) and Lando. This project was setup following this guide: [How to setup Mautic recommended-project with Lando](https://gist.github.com/laurielim/692aeeb7c431a36f84fe1c28df8fc568).

Note that the recommended-project is a production instance and using it for local development isn't advised, see issue '[APP_ENV=dev is not working](https://github.com/mautic/recommended-project/issues/82)'.


## Requirements
You need to have these applications installed to operate on all environments:

- [Docker Desktop](https://www.docker.com/products/docker-desktop/)
- [Lando](https://docs.lando.dev/install.html)

## Create and start the environment

```bash
# Startup the container
lando start

# Install composer packagers
lando composer install

# Import the dump.sql
lando db-import dump.sql

```
Ready! Now go to https://mautic-lando.lndo.site to see your site. Login with `admin:Mautic_Admin1`.


## Useful commands

List information about this app
```bash
lando info
```

Export database
```bash
lando db-export dump.sql
```

Clear cache
```bash
lando mt cache:clear
```

List available commands for Mautic
```bash
lando mt list
```
