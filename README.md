# What is this?

A Quality of Life Discord Package

# Installation

`npm i dishub --save`

# Usage

```js
let Discord = require("discord.js");
let client = new Discord.Client();
let { Say , Re, LOG, Lreply, Edit, Delete } = require('dishub')

client.on("message", message => {

if (message.content === "ping") {
Say(message, "pong!")
}

if (message.content === "ping") {
Re(message, "pong!")
}

if (message.content === "ping") {
LOG("pong!")
}

if (message.content === "ping") {
Lreply(message, "pong!")
}

if(message.content === 'edit')
{
      message.channel.send("hi")
      .then(x => 
      {
          Edit(x, "hehehe", 3000)
          Edit(x, "lol", 5000)
          Edit(x, "xd", 7000)
          Edit(x, "bruh", 9000)
      })
}

if (message.content === "ping") 
{
	Delete(message, "1","pong!", 10000)
}



})

client.login("YOUR TOKEN HERE")
```

**Explanations**
```js
Say(message, "pong!")
```
1. `Say` is the package's Function for normal message.
2. `message` is mesage event where you defined it as message or else. If you defined message event as msg then the code will be like this.
```js
Say(msg, "pong!")
```
3. `"pong!"` or content of thing you wanted to send. It Self-Explanatory.
# Available Options
# Say
Send as normal message

![Code](https://cdn.discordapp.com/attachments/860798919311360030/860799177306931200/unknown.png)
![Output](https://cdn.discordapp.com/attachments/860798919311360030/860799307871813642/unknown.png)
```js
Say(message, 'Content of the message you wanted to send')
```
# Re
Send message with Mention reply

![Code](https://cdn.discordapp.com/attachments/860798919311360030/860799441501421588/unknown.png)
![Output](https://cdn.discordapp.com/attachments/860798919311360030/860799815104069642/unknown.png)
```js
Re(message, 'Content of the message you wanted to send')
```
# LOG
Basically Console.log()

![Code](https://cdn.discordapp.com/attachments/860798919311360030/860800271247605790/unknown.png)
![Output](https://cdn.discordapp.com/attachments/860798919311360030/860800158634344448/unknown.png)
```js
LOG('Content of the message you wanted to send')
```

# Lreply
Sends Message in Form of inline Reply

![Code](https://cdn.discordapp.com/attachments/860798919311360030/860800434389123102/unknown.png)
![Output](https://cdn.discordapp.com/attachments/860798919311360030/860800506179354634/unknown.png)
```js
Lreply(message, 'Content of the message you wanted to send')
```

# Edit
`Edit` function for simplify on editing message using `setTimeout`

![Code](https://cdn.discordapp.com/attachments/828007782221479946/863120884416118834/unknown.png)

1. `message` = The message that will be edited.
2. `content` = The content of next message or message tht will be replace to.
3. `time` = Time to wait till next edits.

```js
Edit(message, content, time[ miliseconds ])
```
# Delete
`Delete` function for simplify on deleting a message after sometime

![Code](https://cdn.discordapp.com/attachments/860798919311360030/863509367155327006/unknown.png)

```js
Delete(message, Option, Content, time[ miliseconds ])
```
1. `message` = The message that will be edited.
2. `Option` `["1", "2", "3", "4"]` = `1` Normal, `2` Reply with mention, `3` lineReply with mention, `4` lineReply Without Mention
2. `content` = The content of next message or message tht will be send.
3. `time` = Time to wait till deletes happen.


