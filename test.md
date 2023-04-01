# Discord Bots × WyldHost
## Introduction
Welcome to WyldHost, the perfect hosting solution for your Discord bot. WyldHost is a powerful and affordable hosting platform that allows you to easily host your Discord bots with ease. In this guide, we'll show you how to set up your Discord bot on WyldHost using Pterodactyl and Node.js.

## Prerequisites
Before we begin, you'll need the following:

- A WyldHost account
- A Discord account
- Basic knowledge of JavaScript
- Getting Started

1. Login to your WyldHost account and create a new server.
2. Upload your bot files to your server. Make sure your main file is named index.js.
3. Install any dependencies your bot needs. You can do this by going to the Startup tab and adding your packages to "Additional Node Modules". (The example Code uses discord.js@13)
4. Start your bot by running node index.js.


## Creating Your Bot

1. Go to the Discord Developer Portal and create a new application.
2. Click on the Bot tab and then click Add Bot.
3. Customize your bot's name and profile picture if desired.
4. Copy your bot token and save it for later.
5. In your bot's code, include the following lines to initialize your bot:


```JS
const { Client, Intents } = require('discord.js');
const client = new Client({ intents: [Intents.FLAGS.GUILDS, Intents.FLAGS.GUILD_MESSAGES] });

client.on('ready', () => {
  console.log(`Logged in as ${client.user.tag}!`);
});

client.on('messageCreate', msg => {
  if (msg.content === 'ping') {
    msg.reply('Pong!');
  }
});

client.login('your-bot-token');
```

6. Customize your bot's behavior by editing the message event listener.

## Conclusion

That's it! Your Discord bot is now hosted on WyldHost and ready to go. If you have any questions or need further assistance, please don't hesitate to contact our support team.
