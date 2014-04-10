### docker-teamspeak3

This is a docker container based on ubuntu with installed Teampspeak 3 server.
Just start the container and its ready to go!

#### Summary
* Ubuntu
* Teamspeak 3 server
* Adding a Licence file (planned)
* make complete ts3 conf accessible (planned)
* settings are persisted between start/stop of the container, after upgrading(using the run cmd to make a new container)
not yet. will follow in the future, probably as an change to the run command, not the dockerfile itself.
#### Usage

  Following commands a just examples which should be ok for most installs.

  * Starting
    
    This starts a docker container in the 
    background (-d) with direct mapping of the TS3 port (-p 9987:9987/udp)
    and sets the name to TS3.

    `sudo docker run --name TS3 -d -p 9987:9987/udp devalx/docker-teamspeak3` 

##### Logs
To get the created Admin secrets use this cmd:

sudo docker logs TS3

you can also specify the container id instead of TS3.

TODO saving data through links neceassry?

##### Settings
This dockerfile can be customized be specifieing several ENV variables.
All of these are optional.
