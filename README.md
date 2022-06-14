# Install operating system on raspberry pi #

go to the [raspberry pi software page](https://www.raspberrypi.com/software/ "raspberry pi software page")

follow the instructions to install the raspberry pi imager.

run the imager and install Raspberry Pi OS Lite.

reboot pi and expand filesystem

# install node #

use the [nodesource debian installation instructions](https://github.com/nodesource/distributions/blob/master/README.md#debinstall "nodesource debian installation instructions") to install the latest version of node.

# install sapphire #

`npm install @sapphire/framework`


# create a sapphire project #

`sapphire new`

give the project a name.

choose typescript for the language.

choose 'default template' for the template.

choose json for the config file.

choose npm for the package manager.

yes to creating a git repository.

# create the bot token #

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

`cd bot_project`

create a password json file

`touch password.json`

edit this content into password.json, replacing BOT_TOKEN with the bot token from the discord developers portal.

`{password: 'BOT_TOKEN'}`



