# An Experimental Alexa Skill for SoundTouch - Local Server Component
## Overview
This repository contains one of the three components necessary enable Alexa to control Bose SoundTouch speakers. The other two required components are:
+ [AlexaSoundTouch\_AlexaSkill](https://github.com/zwrose/AlexaSoundTouch_AlexaSkill) 
+ [AlexaSoundTouch\_RemoteServer](https://github.com/zwrose/AlexaSoundTouch_RemoteServer) 

This Local Server Component tracks presence and activity of SoundTouch speakers on the same network, and communicates with an AlexaSoundTouch\_RemoteServer  instance to broker commands and status updates.

## Setup
These instructions assume you already have spun up or have access to an AlexaSoundTouch\_RemoteServer instance and have created your AlexaSoundTouch\_AlexaSkill instance. They also assume installation on a machine running Ubuntu 14.04 on the same local network as your SoundTouch speakers.

1. Ensure these apt packages are installed: git-core, libnss-mdns, libavahi-compat-libdnssd-dev, build-essential
2. Ensure node v4.x is installed
3. run
    `git clone https://github.com/zwrose/AlexaSoundTouch\_LocalServer.git`
4. Enter the newly cloned directory and run
    `sudo npm install`
5. Edit server.js to set the appropriate bridgeBasePath and bridgeID variables based on your AlexaSoundTouch\_RemoteServer and AlexaSoundTouch\_AlexaSkill instances.
6. run
    `sudo node server.js`

You may choose to use a process manager such as [PM2](https://github.com/Unitech/pm2) to ensure the server stays running.