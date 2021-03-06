# Matrix<->Facebook bridge

Up to date info about Mautrix-facebook itself: https://github.com/tulir/mautrix-facebook

## What?

An Matrix<->Facebook bridge for receiving and sending Facebook messages with Matrix-client, purely for bringing your personal Facebook to your Matrix-client, so you can't mix and bridge Matrix and Facebook users like with most bridges, because there is no known methods in Facebooks side to really do relaybot-like features.

## Set up

### Logging in
- Open chat with `@facebookbot:hacklab.fi`
- Send `login <email> <password>`
- If you have 2FA enabled, the bot will ask you to send the 2FA token.
- Recent chats should now get portals automatically. Other chats will get portals as you receive messages.

### Double puppeting
N.B. Currently only users on the same homeserver as the bridge can log in with their Matrix account.

You can replace the Matrix puppet of your Messenger account with your Matrix account. When you do so, messages that you send from other Messenger clients will be sent from your Matrix account instead of the default puppet user.

Also, until matrix-org/synapse#2954 is fixed, it is the only way to enable bridging of ephemeral events, such as presence, typing notifications and read receipts.

As with the Messenger account login, you must do this in a private chat with the bridge bot.

- Log in with login-matrix <access token>
- After logging in, the default Matrix puppet of your Messenger account should leave rooms and your account should join all rooms the puppet was in automatically.

## Note

Info taken and adapted to our use from [Mautrix-facebook wiki](https://github.com/tulir/mautrix-facebook/wiki/Authentication), so in case of info gets outdated, try refer there.
