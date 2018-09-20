# django lender
django lender

# Version
- Version 1.0.0

# Use


# Features
## Version 1.0.0
- [ ]

## Change Log

### 2018-08-18


# Software
- linux
- Install Docker on Ubuntu 18.04
 - https://www.digitalocean.com/community/tutorials/how-to-install-and-use-docker-on-ubuntu-18-04
```
sudo apt update
sudo apt install apt-transport-https ca-certificates curl software-properties-common
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -
sudo add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/ubuntu bionic stable"
sudo apt update
apt-cache policy docker-ce
# Installed: (none)
sudo apt install docker-ce
sudo apt install docker-compose
sudo systemctl status docker
```
- Installation sucessful
- Setup repo and project
```
mkdir django_lender
git init
pipenv --three
pipenv shell

docker
```
- copy paste basic files.
- https://hub.docker.com/
- https://www.youtube.com/watch?v=pD436N0zw1Y
### Note, do not run docker commands form pipenv
```
touch Dockerfile
sudo docker build -t image_name .
sudo docker image ls
sudo docker image prune
sudo docker stop $(sudo docker ps -a -q)

sudo docker run -d --name container_name -t image_name
sudo docker container ls
sudo docker ps
sudo docker exec -it image_name command
sudo docker exec -it "CONTAINER ID" bash
sudo docker stop my_container
```
### Django
- https://www.djangoproject.com/
```
pipenv shell
pipenv install django psycopg2-binary
django-admin startproject lender_project .
./manage.py runserver
exit
pipenv shell
./manage.py runserver
sudo chmod +x entrypoint.sh
sudo docker-compose up
# To run in backgound
sudo docker-compose up --build &
# To close backgound docker
sudo docker-compose down
```