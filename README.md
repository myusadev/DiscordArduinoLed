# Discord, Arduino and Led
Turn on/off your arduino's led via discord messages, woa!
(arduino ide: am i a joke to you)

```javascript
var jfive = require('johnny-five');
var djs = require('discord.js');
var client = new djs.Client();
    board = new jfive.Board();
board.on("ready", function(){
var led = new jfive.Led(13);
	client.on('message', message => {
		if(message.content == "arduino!led: true"){
			led.on();
      console.log("led: true");
		}
		else if (message.content == "arduino!led: false"){				
			led.off();
      console.log("led: false");
		}
	});
});

client.login('discord-token');
```
<img src="wtfpl.png" alt="WTFPL"/>
