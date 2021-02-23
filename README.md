# Simple discord.js economy system using quick.db
Make a new file/command called beg.js/beg
once the command run(user types the cmd) run this -> 
const db = require('quick.db'); <- this means db = require database(note that some hosting service clear the data)
let amount = await Math.floor(Math.random() * 500);//amount is a random number that is rounded off
let rand = [`${amount}`, 'No'] 
if(rand = amount){
db.add(`${message.author.id}.balance`, amount)//adds the amount
message.channel.send(`You got ${amount} coins from me! Your current balance is ${db.get(`${message.author.id}.balance`)} coins!`)
] else if (rand = `No`){ return message.channel.send("You don't get any money, sorry")}
# Now to the balance cmd
once the command run(user types the cmd) run this -> 
const target = message.mentions.users.first() || message.author //the user that the msg mentioned first or the msg author if no one is pinged
message.channel.send(`<@!${target.id}> has ${db.get(`${target.id}.balance`)} coins!`)
If you want to make a warn system, it's the same but users with administrator can warn a user and adds 1 warn to that user
