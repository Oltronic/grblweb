## About

GRBLweb is a web based GCODE sender and controller for GRBL.  Multiple serial devices can be connected to control multiple machines.

Copyright 2014 Andrew Hodel andrewhodel@gmail.com under the GPL v2 license available in this directory.

## Raspberry Pi prebuilt Image

There is a prebuilt Rasbian image with GRBLweb already running on it at port 80 for 9600 baud GRBL devices.

The ethernet interface will get a DHCP address that you can ssh to.

username: pi

password: password

## GRBL Reading

https://github.com/grbl/grbl

https://github.com/grbl/grbl/wiki/Configuring-Grbl-v0.8

http://onehossshay.wordpress.com/2011/08/21/grbl-how-it-works-and-other-thoughts/

## Config

edit config.js to change serial baud rate and web port

## Installation

```
npm install node-static serialport socket.io
npm install -g forever
```

## Running

// standalone
```
cd grblweb
node server.js
```

// with forever
```
npm install -g forever
cd grblweb
forever start server.js
```

## Access

The default port in config.js is 8000, you can change it by editing the file.

http://hostaddress:8000/
