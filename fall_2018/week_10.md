## Using Docker with a node.js app

This update will include how I have learned to use Docker from working on
OpenCircuits this semester. Hopefully, someone may find this information useful.

From the perspective of a student who wants to get a project up and running on
Docker quickly, the priority is really to treat the Docker container as a brand
new Linux machine which you want to install your app on. In this way, you can
really easily understand how it is to set up your very own Docker image for
your project.

I will be detailing the process we followed when creating the Dockerfile for
OpenCircuits.

For a node.js app, the process is very much simplified due to an already
built catalog of official node.js images. For OpenCircuits, we used the
official image for node 8, yielding the first functional line in the
Dockerfile:

````
FROM node:8
````

Following this, it's easiest to establish a working directory for your
project, as the default work directory is `/`. Then copy your repo
code to the work directory. In the case of OpenCircuits, a web app,
a directory of name `/www` was arbitrarily chosen. Thus:

````
WORKDIR /www
COPY ./ /www
````

The line `RUN sed -i "s/^exit 101$/exit 0/" /usr/sbin/policy-rc.d` was put in
place because we kept getting errors when installing when originally
implementing Docker into the project.

From there, you can install any other dependencies and instruct the image to
execute whatever command on start. In the case of OpenCircuits, these steps
was to install the packages `php` and `php-sqlite3`.

````
RUN apt-get update && apt-get install -y php php-sqlite3
````

Then, as of the refactor,
npm scripts are used to initialize the project and build it. Thus:

````
RUN npm install
RUN npm run init
RUN npm run build
````

And finally, when the project is ready to be run, use the `CMD` command to
set the initial command run at the start of the container to run your
application. In the case for a PHP based project like OpenCircuits:

````
# Change work directory for running php
WORKDIR /www/site/public
CMD php -S 0.0.0.0:8080
````
