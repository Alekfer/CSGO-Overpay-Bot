# CSGO-Overpay-bot

### Setup

```BASH
  CD {the dir of the folder}
  npm i
  node bot.js
```
Then add your ussername,password,secrets and api key to config

TO GET A API KEY GO TO https://steamapi.io/user AND LOGIN WITH STEAM

### Config elements
- `username` AND `password` pretty easy to understand
- `botname` What you want the bots profile name to be, leave blank to not change
- `identitySecret` AND `sharedSecret` You get theese from [Steam Desktop Authenticator](https://github.com/Jessecar96/SteamDesktopAuthenticator/releases/tag/1.0.7.2) and de-crypting the files
- `adminIDs` An array of steam64 ids to auto-accept trades from
- `options`
	- `apiKey` An api key from https://steamapi.io/ as mentioned above
	- `appid` App id to get prices from, 730 (CS:GO) is default not tested to work with others but could
	- `minimumprice` Minium value for their items
	- `acceptRandomFriendRequests` true OR false, easy to understand
	- `priceRefreshInterval` Time (in seconds) to refresh price
	- `confirmationInterval` Time (in seconds) to check mobile auth
	- `percentamount` Percent to value their items at EX: 95% would be 0.95 in config
	- `chatResponse` Chat message handling
		- `donation` Message to send to user when they donate skins
		- `junk` Message to send when users items are less then `minimunprice`
		- `tradeDeclined` Message to send when users items have less value then bots items
		- `tradeAccepted` Message to send when trade goes through
		- `newFriend` Message to send to user when they add the bot
		- `adminTrade` Sent to admin when they make a (auto-accepted) trade to the bot NOTE: admins can be configured in `adminIDs`
		- `commands` Custom simple commands, JSON object in form of "!command"
: "res"





### CONTRBUTING
If you want to contrubuite you must follow theese rules
- Adding elements to config requires you to update README.md
- You must comment your code sufficently
- You have to add enough for it to be merged, EX: i will not merge adding one comment
- Obviously make sure personal details are out of config when makng a PR
- Leave placeholder commands and responces in
- Dont add anything to the bot to scam people