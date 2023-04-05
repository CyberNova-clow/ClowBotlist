# clowbotlist.js
<a href="https://clow.ga/dc" target="_blank"><img src="https://logos-world.net/wp-content/uploads/2020/12/Discord-Logo.png?size=512" alt="Join our discord" width="256"></a><br>
**Support:** [https://clow.ga/dc](https://clow.ga/dc) <br>
**NPM:** [npmjs.com/package/clowbotlist.js](https://www.npmjs.com/package/clowbotlist.js)<br>

## Installation
*If you have trouble with the installation, please feel free to visit our [discord](https://clow.g/dc) address.*
- `npm i clowbotlist.js`

# Define Module & Client
```js
const Discord = require("discord.js");
const client = new Discord.Client();
const clowbotlist = require("clowbotlist.js");
const dbl = new clowbotlist("TOKEN-HERE", client);
//Your Bot Token from clowbotlist 
client.login("BotToken");
```

# Server Count & Shard Count Posting
```js
client.on("ready", async () => {
  dbl.serverCount();
  /* 
  -> Server count posted. 
  or 
  -> Server count & shard count posted.
  */

});
```

# Vote Checking
```js
let hasVote = await dbl.hasVoted("userid"); // -> User ID
  if(hasVote === true) {
      console.log("Voted")
    } else {
      console.log("Vote please.")
  }
// -> Vote please.
```

# Search on clowbotlist
```js
let botFind = await dbl.search("userid");
console.log(botFind.username) // -> Allegro
```
