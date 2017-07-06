# Installing Docker

## Linux

Connect to your Linux machine using a SSH Client such as Putty.

!["Putty SSH Client"](https://github.com/barend-erasmus/installing-docker/raw/master/images/putty.PNG)

We need to start by updating the local server's apt package indexes.

`sudo apt-get update`

Next you'll need to add the GPG (GNU Privacy Guard) key for the Docker repository.

`sudo apt-key adv --keyserver hkp://p80.pool.sks-keyservers.net:80 --recv-keys 58118E89F3A912897C070ADBF76221572C52609D`

We are now authorized to access the Docker repository and it's sources. We can add these sources to our APT sources.

`sudo apt-add-repository 'deb https://apt.dockerproject.org/repo ubuntu-xenial main'`

To make sure that we use the docker-engine package that we just added, we need to update all packages and clear the original docker-engine package from the APT sources.

`sudo apt-get update & apt-cache policy docker-engine`

Installing Docker.

`sudo apt-get install -y docker-engine`

To check if you have successfully installed docker you can run this command.

`sudo systemctl status docker`


## Windows

Go to the [docker site](https://docs.docker.com/docker-for-windows) to download the installer.

Once you have downloaded the installer, run the .msi file.

Follow the installation guide.

After installation you'll have to restart your machine.

To test your docker installation, open command prompt and run the following command:

`docker -v`

You should get an output of `Docker version 1.13.0, build 49bf474` or something similar.