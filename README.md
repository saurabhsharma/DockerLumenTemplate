# Docker Lumen template

This is Docker Lumen Template which you can use to setup your development environment for Lumen Projects.


### Prerequisite	

Before you start make sure you have  [Docker Compose](https://docs.docker.com/compose/install/)  installed on your machine.


### Install

Clone the repo by running the following command

```
$ git clone https://github.com/saurabhsharma/DockerLumenTemplate.git

```

### Config

Before you start your application make sure you have created the file  **.env**  with the correct Docker configuration values. Please take a look into the example on the file  **.env.example**

```
$ mv .env.example .env

```

### Run

To start you application you just need to run the following command

```
$ docker-compose up -d --build

```

### Test

##### 	PHP-FPM

Give it sometime while composer installs all the Lumen dependencies automatically under the vendor folder.

Once it has finished you should be able to see Lumen's default page on your  [browser](http://127.0.0.1/).

##### [](https://github.com/saurabhsharma/docker-lumen-2#php-cli)PHP-CLI

In order to run PHP on the command line you can list all the containers by running

```
$ docker-compose ps

```
Assuming you left the the config value  `COMPOSE_PROJECT_NAME=app`  you should see a container running with the name  **app_workspace_1**

All you have to do is to run the following command to use the workspace container as your main bash

```
$ docker exec -i -t app_workspace_1 /bin/bash

```

And then you will have PHP ready for you, just give it a try!

```
$ php artisan
```
