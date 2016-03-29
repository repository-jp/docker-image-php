# Docker Image for PHP Environment

This repository contains Dockerfile of [PHP](https://secure.php.net/) for [Docker](https://www.docker.com/)'s automated build published to the public [Docker Hub Registry](https://hub.docker.com/).

## Base Docker Image

* [repositoryjp/centos](https://hub.docker.com/r/repositoryjp/centos/)

## PHP Environment

This docker image can create a virtual environment for PHP using [PHPBrew](http://phpbrew.github.io/phpbrew/) and [virtPHP](http://virtphp.org).

When you want to use PHP, run below commands to install PHP that you want to.

[1] Confirm installable versions by PHPBrew.

	phpbrew known

[2] Install PHP 5.6.19 if you needed its version.

	phpbrew install 5.6.19

And you want to create a virtual environment for PHP, run below commands to create its environment.

[Example]

Create a virtual environment named 'php56env' with PHP 5.6.19 when you logged in with the user named 'centos'

	virtphp create --php-bin-dir=/home/centos/.phpbrew/php/php-5.6.19/bin php56env

## PHPBrew Version

* 1.20.6

## virtPHP Version

* 0.5.2

## Installation

1. Install [Docker](https://www.docker.com/).

2. Download automated build from public [Docker Hub Registry](https://hub.docker.com/): `docker pull repositoryjp/php`

## Usage

    docker run -i -t -d -P repositoryjp/php

## About SSH

You can see an user account for ssh at [this repository](https://github.com/repository-jp/docker-image-centos)'s [README](https://github.com/repository-jp/docker-image-centos/blob/master/README.md).

## License

See the file [LICENSE](LICENSE).

## The Author

This Dockerfile was designed and developed by Shinya Kinoshita (From [REPOSITORY](http://www.repositories.jp)) in 2016.
