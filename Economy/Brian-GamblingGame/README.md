<div align="center">

# Gambling Pursuit
A very fun, easy-to-use gambling game made for Atlas.

</div>

## Features

* **Bank space** - Increases overtime whenever you use gambling commands.
* **Boss fights** - Interact with atlas to redeem your win!
* **Customizable** - you have the freedom to modify/control your gameplay.
* **Bug free** - Exploiting is nearly 100% impossible.
* **Currency Shop** - Buy roles, virtual items or everything in your server!
* **Compatability** - The economy system works with 500 or less than members.

## Setup
The game is plug-and-play. Just follow the [`instructions on how to import actions into your server`](../../README.MD). After importing, you can choose from one of the following options to whitelist certain users for them to use the game:

* **Option A** — Running **`a!currency config autoWhitelist true`** automatically whitelists users when they use a currency command. This option is **recommended** so you don't have to spend hours, whitelisting every user in your server manually.
* **Option B** — Whitelist a user manually by running **`a!currency whitelist @user`** and it'll set-up their profile. Leave **`@user`** empty if you wanna whitelist yourself.

---------------------------

### Command Information
The game includes a total of **around 20-25** actions. It works properly when all actions are present. Actions flagged as "important" is the main part of the game which is **required to be added** while actions flagged as "voluntary" are actions that **can or cannot** be added. Even though they can't be added, It's still recommended to add them for a fully functional and efficient system for your server.

> **Legend:** **<>** - required arguments ; **[]** - optional arguments

Command  	| 			Description						| Usage 		   | Flags
:--------: 	| 			:---------: 						| :---: 		   | :---:
**currency** 	| your tool to control the whole currency system 				| `a!currency <...opts>`   | important
**help** 	| leave any command arguments **empty** to view the usage of a command  	| `a!gamble`, `a!give`     | N/A
**balance**	| check your balance or someone else's						| `a!balance @user` 	   | important
**give** 	| give other user some coins, the higher share, the higher tax			| `a!give <amount> @user`  | important
**withdraw** 	| withdraw coins and put it on your pocket					| `a!withdraw <amount>`    | important
**deposit**  	| deposit some coins into your vault						| `a!deposit <amount>`     | important
**gamble**   	| roll a dice and win up to **250%** of your bet				| `a!gamble <amount>`      | important
**slots**    	| use the slot machine to win by matching either **2** or **3** emojis		| `a!slots <amount>`       | voluntary
**flip** 	| take your chances at winning **100%** of your bet by flipping a coin 		| `a!flip <amount>`        | voluntary
**beg**		| ask some random celebrity, some random big company or anyone for coins	| `a!beg`		   | important
**search**	| search for coins somewhere, you can die from it so beware			| `a!search`		   | voluntary
**profile**	| fetch mahority keys from your profile and shows your overall progress		| `a!profile`		   | important
**item**	| view the shop, buy/sell items from the shop or use/deactivate an active item	| `a!item <..opt>`	   | voluntary
**work**	| work for something, you get fired if your gambling stats are weird and bad	| `a!work <[..opt]>`	   | voluntary
**gift**	| gift any amount of any items from your inventory to other users		| `a!gift <#> <item> @user`| voluntary
**trade**	| same as `a!gift` but with a fair interaction to prevent scams			| `a!trade @user <..opt>`  | voluntary

<div id="currency-data-structure">
	
### Data Structure
A user's data includes multiple values. These values are used to interact with the game. The "Key Name" is the name of a [`{perset}`](https://atlas.bot/documentation/tags/perset) while the table below are the values in that perset. You can hack into a perset if you know what you're doing.

> **Key Name:** `{user.id}_data`

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

--------------------------------------
**This superaction was made possible with the help of the following people and tools:**
* [Number Formatter](https://github.com/atlasbot/community-actions/tree/master/Snippets/Emrison-NumberFormatter) - JaM#8608
* <a href="https://regexr.com" target="_blank">regexr.com</a> - My assistant for Regular Expressions
