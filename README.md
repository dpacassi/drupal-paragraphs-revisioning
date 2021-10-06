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
drush cim -y
```

The site can be accessed by [https://dpr.lndo.site/](https://dpr.lndo.site/), (or check your `lando info` output).
