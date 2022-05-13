/*	-WHAT IS THIS?-
	The script featured here is an explanation of how to make your own custom addition to MPMB's D&D 5e Character Tools.
	To add your own content to the Character Sheet, use the syntax below and save it in a file. You can then import this file directly to the sheet using the "Import" button and "Import/Export" bookmark.
	There you can either import the file as a whole or just copy the text into a dialogue.

	-KEEP IN MIND-
	Note that you can add as many custom codes as you want, either by importing consecutive files or pasting the scripts into the dialogue.
	It is recommended to enter the code in a freshly downloaded or reset sheet before adding any other information so that there won't be any conflicts.
*/

/*	-INFORMATION-
	Subject:	Background and Background Feature
	Effect:		This is the syntax for adding a new background and the syntax for adding a new background feature below it
	Sheet:		v12.999 (2017-12-16)
*/

var iFileName = "Homebrew Background - Beauty"; // Optional; This is how the file will be named in the sheet if you import it as a file and not copy-paste its content. Only the first occurrence of this variable will be used
RequiredSheetVersion(12.999); // Optional; This is the minimum required version number of the sheet for the script to work. If the sheet being used to import the script is of an earlier version, the user will be warned

BackgroundList["beauty"] = { //Object name; Note the use of only lower case! Also note the absence of the word "var" and the use of brackets []
	regExpSearch : /beauty/i, //required; regular expression of what to look for (i.e. now it looks for any entry that has the consecutive words "where", "i", "am", and "from" in it, disregarding capitalization or words in between). If this looks too complicated, just write: /where i am from/i

	name : "Beauty", //required; the name as used

	source : ["Backgrounds Omnibus", 3], //required; the source and the page number. "HB" stands for homebrew. See the "Complete SourceList" for an overview of sources that are already defined. Or define a new source using the "Homebrew Syntax - SourceList.js". // This can be an array of arrays to indicate the things appears in multiple sources. For example, if something appears on page 7 of the Elemental Evil Player's Companion and on page 115 of the Sword Coast Adventure Guide, use the following: [["E", 7], ["S", 115]]

	skills : ["Persuasion", "Performance"], //optional; skill proficiencies gained from having the background. If the background doesn't give fixed proficiencies, but instead gives a choice, delete this line and use the line below, "skillstxt"

	gold : 15, //required; the amount of gold pieces added to the Equipment section on the second page when selecting "Background's items and gold" from the "Add Equipment" menu.

	equipleft : [ //optional; syntax is: ["description", "amount", "weight"]. Put "" if it is nothing, don't put 0
		["A hand mirror", "", ""],
		["A token of affection from an admirer", "", ""],
		["A makeup palette or shaving kit", "", ""],
		
	], //items as they are added to the left column of the Equipment section on the second page when selecting "Background's items and gold" from the "Add Equipment" menu.

	equipright : [ //optional; samy syntax as "equipleft"
		["A set of fine clothes", "", 6],
		["Purse (with coins)", "", 1],
	],

	feature : "Enchanting Appearance", //required; the name of the background feature as it will appear on the sheet. The feature is then retrieved from the BackgroundFeatureList, see below

	trait : [
		"There's no shame in using charm to get my way.",
		"What with the impractical outfits I wear into battle, it's a wonder I'm still alive.",
		"I jump at the chance to give anyone a makeover.",
		"I go to great lengths to disguise myself to remain unnoticed.",
		"I'm worried my looks intimidate people. I don't think I'm better than you, I swear!",
		"I strike a pose at any opportunity, even in the midst of battle. I don't realize I do this.",
		"I am stubbornly oblivious about my own attractiveness.",
		"I can't stand grime, so I clean myself obsessively."
	], //required; A list of the personality traits that can be chosen using the "Add Features" button on the second page. This list can be any length.

	ideal : [
		["Charm",
			"Charm: I want to be the embodiment of all that is beautiful. (Any)"
		],
		["Fun",
			"Fun: I want to see how much my looks will let me get away with. (Chaotic)"
		],
		["Control",
			"Control: I gleefully manipulate others to get my way. (Evil)"
		],
		["Inspiration",
			"Inspiration: I want my presence to uplift those around me. (Good)"
		],
		["Expectation",
			"Expectation: I will be exactly what society wants and needs me to be, in fashion and behavior. (Lawful)"
		],
		["Aspiration",
			"Aspiration: I want to as beautiful on the inside as I am on the outside."
		],
	], //required; A list of the  ideals that can be chosen using the "Add Features" button on the second page. This list can be any length. Take note of the two-step build for every ideal, this is essential!

	bond : [
		"I am a close consort to a monarch or noble and I will do whatever I can to honor them.",
		"I am a representative of an organization, hired to advertise them across the known world.",
		"No one takes me seriously as an adventurer because I'm so 'high maintenance'. I will prove them wrong.",
		"An evil person took advantage of me when I was young and naive, and I want revenge.",
		"I seek immortality so that I may stay young and beautiful forever.",
		"A wealthy family only saved me from poverty because of my beauty, but I still owe them my life."
	], //required; A list of the bonds that can be chosen using the "Add Features" button on the second page. This list can be any length.

	flaw : [
		"My looks are superior, so I must be superior in every other way.",
		"Sometimes, my fear of soiling my beauty keeps me from taking risks and doing dirty work.",
		"I expect other people to do things for me.",
		"I have been used too many times fro trust to come easily.",
		"I waste my money on luxuries and pampering.",
		"	I could stare at myself in the mirror all day."
	],  //required; A list of the bonds that can be chosen using the "Add Features" button on the second page. This list can be any length.

/* SYNTAX CHANGE v12.998 >> old syntax for 'tools' and 'languages' are no longer supported!! */
	languageProfs : [2], // optional; this is an array of the language proficiencies gained. An entry can either be 1) a string that represents the language learned or 2) a number which is the number of language gained that can be chosen by the player

	lifestyle : "comfortable", //optional; sets the lifestyle of the sheet. Options are: "wretched", "squalid", "poor", "modest", "comfortable", "wealthy", or "aristocratic"
};

BackgroundFeatureList["enchanting appearance"] = {  //Note the use of only lower case!
	description : "Your appearance causes people who aren't already aggressive or hostile towards you to treat you differently. They will be more willing to interact with you or give you special treatment, especially if they are inclined to be attracted to your gender. However, your interactions are more likely to be misinterpreted as flirtatious. Those who are helping you my attempt romantic overtures, and will be upset if you reject them. Those who see your beauty as a threat may treat you with hostility.", //required; the description of the feature as it will be put on the sheet. Make sure that this fits into the field or it won't look so pretty.

	source : ["Backgrounds Omnibus", 3], //required; the source and the page number of the feature
};
