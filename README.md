# Terraria

Repo to house my Terraria server setup

## Into

I would like to create a simplier way of setting up a terraria server.  The goal would be to have an ansible playbook to control the server, and a var file for terraria settings, maybe cloud hosting vars as well.  I'm going to focus on the linux side of things, and perhaps some improvments to the way terraria saves/backsup.


## Links
I'm mostly followed this guide for setting up.   
[Linode.com](https://www.linode.com/docs/game-servers/host-a-terraria-server-on-your-linode/)

other links
http://ix.io/iHD 
[github.com/Pryaxis](https://github.com/Pryaxis/TShock/releases/tag/v4.3.26)


## Requirments to use
Going to try and keep the requirements pretty light.  I'm going to be using pop!_os 20.04 for my workstation, with virtualbox.  

- Windows or Linux
- [Vagrant](https://www.vagrantup.com/)
- [Virtualbox](https://www.virtualbox.org/wiki/Downloads)


## Quickstart

```shell
chris@pop-os:~/code/terraria$ vagrant up
Bringing machine 'default' up with 'virtualbox' provider...
<output_omitted>
chris@pop-os:~/code/terraria$ vagrant ssh 
<output_omitted>
vagrant@ubuntu-bionic:~$ sudo -i
root
```
<script id="asciicast-VGJFCbXpXVOkO9N87XIEVoTCV" src="https://asciinema.org/a/VGJFCbXpXVOkO9N87XIEVoTCV.js" async></script>

### other notes. 

Sad to find out that they have removed old versions from the site. Not 100% sure i can correctly test installing by specifiying a version.  
I'm curious to test with a couple different configurations. Right now I guess i'm manually testing via logging in through my gaming machine.  
