# mineflayer-tps

A mineflayer plugin to easy get the server tps!
You can install from [npm](https://www.npmjs.com/package/mineflayer-tps).

## Usage

Look at [this](https://github.com/SiebeDW/mineflayer-tps/blob/master/examples/gettps.js).

Or simple:
```js
var mineflayer = require('mineflayer')
var tpsPlugin = require('mineflayer-tps')(mineflayer)

var bot = mineflayer.createBot()

bot.loadPlugin(tpsPlugin) // Load the plugin

// Example how to use
bot.on('chat', (username, message) => {
  if (username === bot.username) return
  if (message === 'tps') {
    bot.chat('Current tps: ' + bot.getTps())
  }
})

```
