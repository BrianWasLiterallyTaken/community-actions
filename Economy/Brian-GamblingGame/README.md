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
The game is plug-and-play. Just follow the [`instructions on how to import actions into your server`](../../README.MD). When whitelisting, you can choose from one of the following options:

* **Option A** — Running **`a!currency config autoWhitelist true`** automatically whitelists users when they use a currency command. This option is **recommended** so you don't have to spend hours, whitelisting every user in your server manually.
* **Option B** — Whitelist a user manually by running **`a!currency whitelist @user`** and it'll set-up their profile. Leave **`@user`** empty if you wanna whitelist yourself.

### Command Information
The game includes a total of **around 20-25** actions. It works properly when all actions are present. Actions flagged as "important" is the main part of the game which is **required to be added** while actions flagged as "voluntary" are actions that **could not** be added. Even though they can't be added, It's still recommended to add them for a fully functional, efficient and a nice addition for your server.
> **Legend:** **<>** - required arguments \| **[]** - optional arguments

Command  | Description | Usage | Requires Whitelist
:------: | :---------: | :---: | :----------------:
currency | this will serve as your tool to control the currency system | `a!currency <...opts>` | false
help 	 | trigger the help menu by leaving any command arguments **empty**| `a!gamble`, `a!give` | true
balance	 | checks your or someone else's balance | `a!balance @user` | true
give 	 | gives other user coins | `a!give <amount> @user` | true
withdraw | withdraw coins from your bank | `a!withdraw <amount>` | true
deposit  | deposit coins to your bank | `a!deposit <amount>` | true
gamble   | roll a dice and win | `a!gamble <amount>` | true
slots    | use the slot machine to win a jackpot price | `a!slots <amount>` | true
flip 	 | flip a coin! | `a!flip <amount>` | true

<div id="currency-data-structure">
	
### Data Structure
A user's data includes multiple values. These values are used to interact with the game. The "Key Name" is the name of a [`{perset}`](https://atlas.bot/documentation/tags/perset) while the table below are the values in that perset. You can hack into a perset if you know what you're doing.
> **Key Name**\
`{user.id}_data`

    Key	   	| 		Description 		    	  	  | Default Value 
   :---:   	| 		:---------: 		    	  	  | :-----------: 
**Pocket** 	| The amount used for buying items and gambling coins  	  | **`50,000`**
**Vault**  	| A *safe* place to store user coins	   	  	  | **`100,000`**
**Space**  	| The capacity of a user's vault		  	  | **`100,000`**
**Gems**   	| Coins but in other currency type to buy premium items	  | **`150`**
**Multiplier**  | The **base rate** of how much the winnings are	  | **`5%`**
**Experience**  | Experience **points** you've already earned 	  	  | **`1`**
**Wins**	| How many **times** you've **lost** from games	  	  | **`0`**
**Loses**	| How many **times** you've **won** from games    	  | **`0`**
**Won**		| Overall amount you've **spent** and **lost** from games | **`0`**
**Lost**	| Overall amount you've **lost** from games	  	  | **`0`**
**Whitelisted** | The state; either blocked, banned or true 	  	  | **`true`**

</div>

### Credits
The superaction was made possible with the help of the following:
* [Number Formatter](https://github.com/atlasbot/community-actions/tree/master/Snippets/Emrison-NumberFormatter) - JaM#8608
* <a href="https://regexr.com" target="_blank">regexr.com</a> - My assistant for Regular Expressions
