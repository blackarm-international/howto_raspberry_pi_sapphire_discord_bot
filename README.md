# Install operating system on raspberry pi #

go to the [raspberry pi software page](https://www.raspberrypi.com/software/ "raspberry pi software page")

follow the instructions to install the raspberry pi imager.

run the imager and install Raspberry Pi OS Lite onto the sd card. (pi 3 needs 32 bit version)

put the sd card in the pi.

connect pi to keyboard, monitor.

power up.

# configure pi

find the user name

`whoami`

start the raspberry pi config tool

`sudo raspi-config`

- change password

- set the hostname (this will show up in nmap)

- enable ssh

shut the pi down

`sudo shutdown -h now`

# connect pi to network and ssh in

plug the pi into the router

connect the power supply

find the pi's ip address with nmap

`nmap -sS -p 22 192.168.1.0/24`

connect with ssh (replace the xxxs with username and ip)

`ssh xxxxxxxx@192.168.1.XXX`

# install node #

use the [nodesource debian installation instructions](https://github.com/nodesource/distributions/blob/master/README.md#debinstall "nodesource debian installation instructions") to install the latest version of node.

`curl -fsSL https://deb.nodesource.com/setup_18.x | bash -`<br/>
`apt-get install -y nodejs`

# install sapphire #

`npm install @sapphire/framework`


# create a sapphire project #

`sapphire new`

name the project testbot.

choose typescript for the language.

choose 'default template' for the template.

choose json for the config file.

choose npm for the package manager.

yes to creating a git repository.

# modify the code

go into the code folder

`cd testbot`

create a json password file (this will be edited later)

`echo '{token: "BOT_TOKEN"}' > config.json`

edit index.ts

`nano index.ts`

add this line at the start

**const botData = require('./config.json');**

change this line

**client.login();**

to

**client.login(botData.token);**

# create the bot in the discord developers portal #

go to the [discord developers portal](https://discord.com/developers/applications)

click on 'applications' on the left hand menu.

click on 'new application'.

create a new application.

click on the newly created application.

click on 'bot' in the left hand menu.

copy the bot token.

--- some more stuff ----

# modify your project to connect to the bot #

cd into your sapphire project

***cd bot_project***

create a password json file

***touch password.json***

edit this content into password.json, replacing BOT_TOKEN with the bot token from the discord developers portal.

`{password: 'BOT_TOKEN'}`



