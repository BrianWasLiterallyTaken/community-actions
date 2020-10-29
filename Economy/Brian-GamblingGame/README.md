<div align="center">

# Gamble
A very fun, easy-to-use gambling game made for Atlas.

</div>

## Features

* **Bank space** - Increases overtime whenever you use gambling commands.
* **Boss fights** - Interact with atlas to redeem your win!
* **Customizable** - you have the freedom to modify/control your gameplay.
* **Bug free** - Exploiting is nearly 100% impossible.
* **Currency Shop** - Buy roles, virtual items or everything in your server!
* **Compatability** - The economy system works with 500 or less than members.

### Setup

1. In order for users to use those commands, make sure you whitelist them (and yourself of course) using the following command:
	* `a!currency whitelist @user` (Optional: leave @user empty if you'll whitelist yourself)
	* This will create a key named `{user.id}_data` on your persistent storage. See <a href="#currency-data-structure">an example</a> of a key with other info about it as well.
	```yaml
	Pocket: 50000
	Vault: 100000
	Space: 100000
	
	Multiplier: 5
	Experience: 1
	
	Wins: 0
	Loses: 0
	Won: 0
	Lost: 0

	Whitelisted: true
	```
	* `Pocket` starts off with `50,000` coins
	* `Vault` and `Space` starts off with `100,000` coins equally for both values
	* `Multiplier` is our base rate of how high or low your winnings are
	* `Experience` whenever you reach a specific level, you gain a random multiplier
	* `Wins` how many times you've won a game of gamble or slots
	* `Won` overall coins you've won from games
	* `Loses` how many times you lost a game of gamble or slots
	* `Lost` overall coins you've lost from games
4. You're now done! You can now play the game.


### Command Information
> **Legend**\
**<>** - required arguments\
**[]** - optional arguments

Command | Description | Usage | Permissions | Requires Whitelist
:---: | :---: | :---: | :---: | :---:
currency | this will serve as your tool to control the currency system | `a!currency <...opts> @user` | Manage Server | false
help | trigger the help menu by leaving any command arguments **empty**| `a!gamble`, `a!give` | Send Messages | true
balance | checks your or someone else's balance | `a!balance <optionalUser>` | Send Messages | true
give | gives other user coins | `a!give <amount> @user` | Send Messages | true
withdraw | withdraw coins from your bank | `a!withdraw <all \| max \| amount>` | Send Messages | true
deposit | deposit coins to your bank | `a!deposit <all \| max \| amount>` | Send Messages | true
gamble | roll a dice and win | `a!gamble <amount \| all \| max \| half \| 69k>` | Send Messages | true
slots | use the slot machine to win a jackpot price | `a!slots <amount \| all \| max \| half \| 69k>` | Send Messages | true

### <div id="currency-data-structure">### Data Structure</div>

### Credits
* [Number Formatter](https://github.com/atlasbot/community-actions/tree/master/Snippets/Emrison-NumberFormatter) - JaM#8608
* <a href="https://regexr.com" target="_blank">regexr.com</a> - My lovely assistant for Regular Expressions.
