# DiscordBot-JS Tutorial
### We will not spoon feed you.

# Requirements
* A brain. [View](https://i.ytimg.com/vi/kcMt_Rc6ZLs/maxresdefault.jpg)
* Visual Studio Code [Download](https://code.visualstudio.com/download)
 
# Environment
Once you have a code editor installed, open command prompt and follow along.

### Navigate
```
cd {DIRECTORY YOU CREATED FOR YOUR BOT}
```
### Install nodejs/discord.js
```
npm install nodejs
npm install discord.js
npm install fs
```
### Getting The Basic Bot Code Together
```js
// Make sure to create the 'botconfig.json' file.
const botconfig = require("./botconfig.json");

// Pulls the discord api in to be used.
const Discord = require("discord.js");

// Declares constant 'bot' as a new discord client from api.
const bot = new Discord.Client();

// Declares our message prefix from 'botconfig.json'
const prefix = botconfig.prefix;

// Tells us whether the bot is ready
bot.on("ready", async () => {

// Tells us our bot is online.
console.log('Bot Tutorial By Root on Discordian: ONLINE');

// Lets set an acitivty, displays under the bot.
bot.user.setActivity("v1.0");

// Ends the ready function.
});

// Creates general contstant for when messages are sent.
bot.on('message', message => {

// Arguments entered by a user.
const argument = message.content.trim().split(/ +/g);

// Command being sliced then used if it has an argument.
const command = args[0].slice(prefix.length).toString();

// Example command with arguments.
let sentence = argument[0]; // Declares what the user entered without the command.

// Example: !hi Display this | Output: Display this
if (command == "hi") {

// Send the enterered sentence back
message.channel.send(sentence);

// Ends the if commmand.
}

// Ends the constant for messages.
});

// Bot logins with verification token from discord developer panel.
bot.login(botconfig.token);
```
# Creating The botconfig.json File
Don't just copy and paste, actually learn from this.

### Code Example
```json
{
 "token": "TOKEN GOES HERE",
 "prefix": "!"
}
```
# Running Your Bot/Controls
```
cd {BOT LOCATION}
```
### Type: node index.js - Starts the bot.
### Ctrl-C - Stops the bot.

As far as getting the token from the discord developer panel and setting permissions is on you, as if you don't know how to click and add the bot to your channel this tutorial probably isn't for you.

# [Join Our Community For More! => CLICK HERE ](https://discord.gg/ZpdzcyFTSR)
