# Drupal Paragraphs Revisioning

## Installation
Install [Lando](https://lando.dev/).

Then run:
```
git clone git@github.com:dpacassi/drupal-paragraphs-revisioning.git
cd drupal-paragraphs-revisioning
cp .env.example .env
lando start
```

Run `lando ssh` to SSH into the container and then:

```
cd /app
composer install
cd web
drush cr
drush site:install --existing-config -y
drush cr
drush cim -y
drush cr
```

Note that specially the `drush site:install` command will take a few minutes, so when running that command, it's a
good time to get yourself a coffee :)
After that command you also received the login credentials for the user 1. As an alternative, there's always
`drush uli 1`.

The site can be accessed by [https://dpr.lndo.site/](https://dpr.lndo.site/), (or check your `lando info` output).
