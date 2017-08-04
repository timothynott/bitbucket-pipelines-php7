# Bitbucket Pipelines PHP 7.1 image

## Based on [Official PHP image](https://hub.docker.com/_/php/) and work done by [Eduardo Bizarro](https://github.com/edbizarro/)

### Packages installed

- PHP 7.1 with `mcrypt`, `mongod`, `xdebug`, `zip`, `xml`, `mbstring`, `curl`, `json`, `imap`, `mysql`, `iconv`, `gd`, `pdo_mysql`, `opcache`, `intl`. `zip`, `bcmath` and `tokenizer`
- [Composer](https://getcomposer.org/)
- Node 8.x / NPM / Gulp / [Yarn](yarnpkg.com)

## `bitbucket-pipelines.yml` example

```YAML
image: edbizarro/bitbucket-pipelines-php7
pipelines:
  default:
    - step:
        script:
          - npm install
          - composer install --no-interaction --no-progress --prefer-dist
          - rsync some stuff
```
