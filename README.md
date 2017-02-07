# chat-linker

> linker for chats from different networks

![illustration](https://cloud.githubusercontent.com/assets/1261240/22682361/5491e34c-ed23-11e6-83fe-ce50c18cdb13.png)

## Using

### Setting
Copy `sample-config.json` to `app-config.json` and tune it up.

To determine Telegram room parameters, follow the procedure:

1. Create a bot according to [Telegram documentation][bots-docs]
2. Manually add a bot to the room (using Telegram's invite functionality)
3. Send a message to the bot **directly**, e.g. `/my_id @bot_user_id`
4. Visit `https://api.telegram.org/bot<bot_api_key>/getUpdates` and extract
   `"chat"` object from there. E.g.

   ```json
   {
       "id": -1001054401089,
       "title": "bimo_test",
       "type": "supergroup"
   }
   ```
5. To make all room messages visible to the bot, make it a room admin

### Run

To start the bot:

+ Use the commands `npm run prod` for production settings or `npm run dev` for development.

## Contribution

### Tests

To run tests use following command:

```sh
npm test

```

### Setting up husky

If after the installation does not work git-hooks then run the following command in project directory.

```sh
node ./node_modules/husky/bin/install.js
```

### Discussion

- telegram: [javascript_ru](https://t.me/javascript_ru) (RU)
- jabber: [javascript@conference.jabber.ru](xmpp://javascript@conference.jabber.ru) (RU)


[bots-docs]: https://core.telegram.org/bots#3-how-do-i-create-a-bot
