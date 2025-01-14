@erupcja/selfbot-eris
====

A fork of [`eris`](https://abal.moe/Eris), a NodeJS wrapper for interfacing with Discord.

Installing
----------

You will need NodeJS 8+. If you need voice support you will also need Python 2.7 and a C++ compiler. Refer to [the Getting Started section of the docs](https://abal.moe/Eris/docs.html) for more details.

```
npm install --no-optional @erupcja/selfbot-eris
```

If you need voice support, remove the `--no-optional`

Ping Pong Example
-----------------

```js
const Eris = require("@erupcja/selfbot-eris");

var bot = new Eris("BOT_TOKEN");
// Replace BOT_TOKEN with your bot account's token

bot.on("ready", () => { // When the bot is ready
    console.log("Ready!"); // Log "Ready!"
});

bot.on("messageCreate", (msg) => { // When a message is created
    if(msg.content === "!ping") { // If the message content is "!ping"
        bot.createMessage(msg.channel.id, "Pong!");
        // Send a message in the same channel with "Pong!"
    } else if(msg.content === "!pong") { // Otherwise, if the message is "!pong"
        bot.createMessage(msg.channel.id, "Ping!");
        // Respond with "Ping!"
    }
});

bot.connect(); // Get the bot to connect to Discord
```

More examples can be found in [the examples folder](https://github.com/abalabahaha/eris/tree/master/examples).

Useful Links
------------

[Chat with the fork author on Matrix](https://matrix.to/#/#erupcja-selfbot-eris:laura.pm)

[The website](https://abal.moe/Eris) includes more detailed information on getting started, as well as documentation for the different components.

[The Discord API channel (#js_eris)](https://abal.moe/Eris/invite) is the best place to get support/contact the original module author.

[The original GitHub repo](https://github.com/abalabahaha/eris) has the most updated code.

[The NPM package](https://npmjs.com/package/@erupcja/selfbot-eris)

License
-------

Refer to the [LICENSE](LICENSE) file.
