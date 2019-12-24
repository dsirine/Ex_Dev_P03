## Installation de VM ##

Afin de mettre en place une machine virtuelle, vous utiliserez l'outil Vagrant, qui permet de décrire et de manipuler très facilement les différents éléments de votre environnement: \
    $ sudo apt install virtualbox \
    $ sudo apt install vagrant \
    $ vagrant --version \
    $ mkdir EX_Dev_P03 \
    $ cd EX_Dev_P03 \
    $ vagrant init ubuntu/bionic64 \
    $ vagrant up \
    $ vagrant ssh

## Installation environnement de travail ##

Vous allez maintenant installer des outils dans votre VM Vagrant. Faites évoluer votre Vagrantfile, et ajoutez les lignes nécessaires pour ajouter : \
    - Un éditeur de texte Vim. \
    - Ansible. \
    - Docker Community Edition

## Une serveur Nginx ##

Votre image contiendra un serveur nginx, et devra donc également être accessible en HTTP : \
    - création un fichier Dockerfile dans la VM ainsi le fichier default de configuration \
    $ docker build -t nginx . \
    $ docker images \
    $ docker run -d -p 80:80 nginx \
    $ docker ps \
    $ sudo ufw allow 80 \
    $ curl localhost \
    - forwarding les ports hosts et guest
