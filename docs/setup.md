# 🛠️ Setting up the bot
**Note:** This bot can run on your PC or in https://replit.com
I recommend using replit.com to run and https://uptimerobot.com to host 24/7 for free
To keep it online, you need to keep the bot process running.

## Terminology
* **Main server** (or main guild) is the server where users will be contacting modmail from
* **Inbox server** (or inbox guild, or mail guild) is the server where modmail threads will be created.
  In a "single-server setup" this is the same server as the main server.
* A **modmail thread** is a channel on the **inbox server** that contains the current exchange with the **user**.
  These threads can be closed to archive them. One **user** can only have 1 modmail thread open at once.
* A **moderator**, in modmail's context, is a server staff member who responds to and manages modmail threads
* A **user**, in modmail's context, is a Discord user who is contacting modmail by DMing the bot

## Prerequisites
1. Create a bot on the [Discord Developer Portal](https://discord.com/developers/applications)
2. Turn on **Server Members Intent** in the bot's settings page on the developer portal ([Image](server-members-intent-2.png))
3. Then go to replit.com and click on New REPL and click on IMPORT FROM GITHUB then paste the link of this repository.

## Setup
In this setup, modmail threads are opened on the main server in a special category.
This is the recommended setup for small and medium sized servers.

1. **Go through the [prerequisites](#prerequisites) above first!**
2. Open `config.ini` in your repl and fill in the required values. `mainServerId` and `inboxServerId` should both be set to your server's id.
3. Invite the bot to the server.
4. On a new line at the end of `config.ini`, add `categoryAutomation.newThread = CATEGORY_ID_HERE`
    * Replace `CATEGORY_ID_HERE` with the ID of the category where new modmail threads should go
5. Make sure the bot has `Manage Channels`, `Manage Messages`, and `Attach Files` permissions in the category
    * It is not recommended to give the bot Administrator permissions under *any* circumstances
6. Then click on RUN button and then when a website-like scren pops up, copy its link.
7. Then go to https://uptimerobot.com and Register if u didn't and Login if u did. Then go to Dashboard page and click on New Monitor. there select monitor type as HTTP(s) and paste the link of the repl u copied. Then scroll down and click on create monitor and again click it. Now your Bot will run 24/7 for Free. 
8. Want to change other bot options? See **[📝 Configuration](configuration.md)**
9. Have any other questions? Check out the **[🙋 Frequently Asked Questions](faq.md)** or
   **[join the support server!](../README.md#support-server)**


*\* Since all channel names, even for channels you can't see, are public information through the API, a user with a
modified client could see the names of all users contacting modmail through the modmail channel names.* 
