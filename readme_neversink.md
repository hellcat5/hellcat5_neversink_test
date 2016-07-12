# Creation Date: 20160712
# Created By: Neversink refactored by Hellcat5
#----------------------------------------------------------
# comments regarding refactoring each section listed below
#----------------------------------------------------------
# Defined consistent condition order:
#
BaseType <Type>						- BaseType must be capitalized (Sabre not sabre)
Class	<Class>						- Class must be capitalized (Sword not sword)
LinkedSockets [Operator] <Links>	- (0, 2-6)
Sockets [Operator] <Sockets>		- (0-6)
SocketGroup [Group]					- RGB or RGBBWW etc.
Height [Operator] <Value>			- (1-4)
Width [Operator] <Value>			- (1-2)
Rarity [Operator] <Rarity> 			- (Normal, Magic, Rare, Unique)
Quality [Operator] <Quality>		- (0-20)
DropLevel [Operator] <Level>		- (0-100)
ItemLevel [Operator] <Level>		- (0-100)
#
# Defined consistent action order:
#
SetFontSize <FontSize>
SetTextColor <Red> <Green> <Blue> [Alpha]
SetBorderColor <Red> <Green> <Blue> [Alpha]
SetBackgroundColor <Red> <Green> <Blue> [Alpha]
PlayAlertSound <Id> [Volume]
#
#----------------------------------------------------------
#
# ALPHA # GLOBAL OVERRIDE - ADD YOUR OWN RULES THAT WILL OVERRIDE THE OTHERS HERE
# ALPHA-a # Talisman league!
 - removed explicit declaration of inherited property value (alpha transparency) - SetBorderColor 109 200 130 (255)
 - removed explicit declaration of inherited property value (default color declaration and alpha transparency) - (SetBackgroundColor 0 0 0 255)
 - font size change - (SetFontSize 42) SetFontSize 44
 - font size change - (SetFontSize 38) SetFontSize 36
 - font size change - (SetFontSize 36) SetFontSize 32
 
# 0000 # UTILITY AND JUST-IN-CASE
 - no change
 
# 0001 # LABYRINTH MATERIAL
 - removed explicit declaration of inherited property value (alpha transparency) - SetBackgroundColor 180 0 0 (255)
 - removed explicit declaration of inherited property value (default color declaration) - (SetBorderColor 0 0 0)

# 0100 # TOP TIER RARITY
 - font size change - (SetFontSize 45) SetFontSize 44
 - font size change - (SetFontSize 43) SetFontSize 40
 - removed explicit declaration of inherited property value (alpha transparency) - SetTextColor 255 0 0 (255)
 - removed explicit declaration of inherited property value (alpha transparency) - SetBorderColor 255 0 0 (255)
 - removed explicit declaration of inherited property value (alpha transparency) - SetBackgroundColor 255 255 255 (255)

# 0200 # UNIQUES AND MAPS

# 0201 # UNIQUE TIER LIST
 - font size change - (SetFontSize 45) SetFontSize 44
 - removed explicit declaration of inherited property value (default color declaration and alpha transparency) - (SetBorderColor 0 0 0 255)
 - removed explicit declaration of inherited property value (alpha transparency) - SetTextColor 0 0 0 (255)
 - removed explicit declaration of inherited property value (alpha transparency) - SetBackgroundColor 200 96 37 (255)
 - font size change - (SetFontSize 43) SetFontSize 40
 - font size change - (SetFontSize 39) SetFontSize 36

# 0202 # MAP TIER LIST
 - corrected precedence issue with tier order
 - removed explicit declaration of inherited property value (default color declaration and alpha transparency) - SetBorderColor 0 0 0 255 
 - removed explicit declaration of inherited property value (alpha transparency) - SetTextColor 0 0 0 (255)
 - removed explicit declaration of inherited property value (alpha transparency) - SetBackgroundColor 200 200 200 (255)
 - font size change - (SetFontSize 45) SetFontSize 44
 - font size change - (SetFontSize 43) SetFontSize 40
 - font size change - (SetFontSize 42) SetFontSize 40
 - font size change - (SetFontSize 41) SetFontSize 40
 - font size change - (SetFontSize 38) SetFontSize 36
 - font size change - (SetFontSize 36) SetFontSize 32
 - font size change - (SetFontSize 35) SetFontSize 32
 - font size change - (SetFontSize 34) SetFontSize 32
 - removed commented out actions (this is an active filter, not a filter template)
 - reduced redundant statements regarding lower tier map drops (merged t6 to t1 into one block)
 - Map colorations:
 - Tiers 1-6 - white - 1 block definition
 - Tiers 7-11 - gold - 2 block definitions
 - Tiers 12-15 - red - 3 block definitions
 
# 0203 # MAP FRAGMENTS
 - font size change - (SetFontSize 45) SetFontSize 44
 - removed explicit declaration of inherited property value (default color declaration and alpha transparency) - SetBorderColor 0 0 0 255
 - removed explicit declaration of inherited property value (alpha transparency) - example: SetTextColor 0 0 0 (255)
 - font size change -  (SetFontSize 38) SetFontSize 36
 
# 0300 # CURRENCY
# 0301 # TOP TIER: DIVINE, EXALTED
 - font size change - (SetFontSize 45) SetFontSize 44
 
# 0302 # HIGH TIER: FROM ALCHEMY TO REGAL
 - removed explicit declaration of inherited property value (default color declaration and alpha transparency) - SetBorderColor 0 0 0 255 

# 0303 # MEDIUM-LOW ORBS
 - removed explicit declaration of inherited property value (default color declaration and alpha transparency) - SetBorderColor 0 0 0 255 

# 0304 # BOTTOM TIER: LOW ORB VARIATIONS
 - font size change -  (SetFontSize 28)	SetFontSize 28
 
# 0305 # DIVINATION CARD TIER LIST
 - font size change - (SetFontSize 45) SetFontSize 44
 - font size change - (SetFontSize 38) SetFontSize 36
 - removed explicit declaration of inherited property value (alpha transparency) - example: SetBorderColor 0 0 255 (255)

# 0306 # SPECIAL CURRENCY
 - font size change - (SetFontSize 38) SetFontSize 36

# 0307 # REST
 - removed below duplicate entry. Reason Class searches for all matching elements, thus Currency and Stackable Currency included:
 Show
	Class Stackable Currency
	SetBorderColor 0 0 0 255

#commented out due to explicit definition of inherited values
#Show
#	Class Currency
#	SetBorderColor 0 0 0 255	


# 0400 # SOCKET/LINK BASED stuff
 - font size change - (SetFontSize 39) SetFontSize 40
 
# 0500 # SKILL GEMS
 - removed explicit declaration of inherited property value (alpha transparency) - example: SetTextColor 30 150 180 (255)
 - font size change - (SetFontSize 45) SetFontSize 44
 - font size change - (SetFontSize 38) SetFontSize 36
 - font size change - (SetFontSize 41) SetFontSize 40
 
# 0600 # RARE ITEM HIGHLIGHTING

# 060a # RARES SUITABLE FOR ENDGAME CRAFTING
 - removed explicit declaration of inherited property value (alpha transparency) - example: SetBorderColor 255 255 0 (255)
 - font size change - (SetFontSize 38) SetFontSize 36
 
# 060b # RARE RINGS, AMULETS, JEWELS, BELTS
 - font size change - (SetFontSize 39) SetFontSize 40
 
# 060c # DROP LEVEL 69+ ITEMS ARE ALWAYS PRIORITIZED RARES
 - font size change - (SetFontSize 35) SetFontSize 36

# 0601 # RARE DAGGERS
 - font size change - (SetFontSize 35) SetFontSize 36

# 0602 # RARE CLAWS
 - font size change - (SetFontSize 35) SetFontSize 36

# 0603 # RARE WANDS
 - font size change - (SetFontSize 35) SetFontSize 36

# 0604 # RARE SWORDS
 - font size change - (SetFontSize 35) SetFontSize 36
 - removed explicit declaration of inherited property value (color) - example:	(SetBorderColor 0 0 0)

# 0605 # RARE AXES&MACES (1H)
 - font size change - (SetFontSize 35) SetFontSize 36
 - removed explicit declaration of inherited property value (color) - example:	(SetBorderColor 0 0 0)
 
# 0606 # RARE SCEPTRES
 - font size change - (SetFontSize 35) SetFontSize 36
 - removed explicit declaration of inherited property value (color) - example:	(SetBorderColor 0 0 0)

# 0607 # RARE STAVES
 - font size change - (SetFontSize 35) SetFontSize 36
 - removed explicit declaration of inherited property value (color) - example:	(SetBorderColor 0 0 0)
 
# 0608 # RARE TWO HAND SWORDS + MACES + AXES
 - font size change - (SetFontSize 35) SetFontSize 36
 - removed explicit declaration of inherited property value (color) - example:	(SetBorderColor 0 0 0)

# 0609 # RARE BOWS
 - font size change - (SetFontSize 35) SetFontSize 36
 - removed explicit declaration of inherited property value (color) - example:	(SetBorderColor 0 0 0)

# 0610 # RARE QUIVERS
 - font size change - (SetFontSize 35) SetFontSize 36
 - removed explicit declaration of inherited property value (color) - example:	(SetBorderColor 0 0 0)

# 0611 # RARE GLOVES, HELMETS, BOOTS
 - font size change - (SetFontSize 35) SetFontSize 36
 - removed explicit declaration of inherited property value (color) - example:	(SetBorderColor 0 0 0)

# 0612 # RARE SHIELDS

 - font size change - (SetFontSize 31) SetFontSize 32
 - removed explicit declaration of inherited property value (color) - example:	(SetBorderColor 0 0 0)

# 0613 # RARE BODY ARMOR
 - font size change - (SetFontSize 35) SetFontSize 36
 - removed explicit declaration of inherited property value (color) - example:	(SetBorderColor 0 0 0)

# 0614 # RARES - LEVELING SPECIFIC RULES
 - font size change - (SetFontSize 35) SetFontSize 36
 - font size change - (SetFontSize 39) SetFontSize 40
 - font size change - (SetFontSize 37) SetFontSize 36
 - font size change - (SetFontSize 35) SetFontSize 32
 - removed explicit declaration of inherited property value (color) - example:	(SetBorderColor 0 0 0)

 # 0615 # RARES - REMAINING RULES
 - font size change - (SetFontSize 31) SetFontSize 32
 
# 0700 # NORMAL AND MAGIC ITEM RULES
 - font size change - (SetFontSize 38) SetFontSize 36
 
# 0701 # 83+ ITEM CRAFTING
 - font size change - (SetFontSize 38) SetFontSize 36

# 0702 # CHROMATIC ORB RECIPE ITEMS

# 0703 # CHANCE ORB BASES - ADD YOUR ITEMS HERE
 - font size change - (SetFontSize 38) SetFontSize 36

# 0704 # HIGH LEVEL WHITE RINGS/AMULETS FOR ALCHING

# 0705 # MAGIC RINGS, AMULETS, BELTS

# 0706 # MAGIC JEWELS

# 0707 # CHISEL RECIPE ITEMS
 - font size change - (SetFontSize 38) SetFontSize 36

# 0708 # HIGH LEVEL 4+ LINKED ITEMS

# 0709 # TOP BASES FOR CRAFTING
 - removed redundant code - instead, just add the BaseType you wish to search for to the BaseType line

# 0710 # MARAKETH WEAPONS
 - removed redundant code - instead, just add the BaseType you wish to search for to the BaseType line

# 0711 # PRE-ENDGAME 20% QUALITY ITEMS

# 0712 # ANIMATE WEAPON SCRIPT (DISABLED)

# 0800 # FLASKS
 - removed explicit declaration of inherited property value (alpha transparency) - SetTextColor 255 255 255 (255)
 - font size change - (SetFontSize) 38 SetFontSize 36 

# 0801 # HIDE OUTDATED FLASKS
# 0802 # HIDE NON-QUALITY RANDOM FLASK DROPS IN MAPS
# 0803 # FLASKS - Hybrid Flasks (Normal)
# 0804 # FLASKS - Hybrid Flasks (Magic)
# 0805 # FLASKS - HIGHLIGHT NEW NORMAL FLASKS (Kudos to Antnee)
# 0806 # FLASKS - HIGHLIGHT NEW MAGIC FLASKS (Kudos to Antnee)

# 0807 # SHOW WHATEVER FLASKS REMAIN
 - font size change - (SetFontSize 29) SetFontSize 28

# 0900 # LEVELING
# 0901 # LEVELING HIGHLIGHT JEWELRY

# 0902 # HIGHLIGHT LEVELING SPECIFIC ITEMS
 - font size change - (SetFontSize 36) SetFontSize 38
 - removed redundant code:
 Show
	Class "Sceptres" "Wands"
	Rarity = Magic
	ItemLevel < 25
	SetFontSize 36
	SetBorderColor 100 100 100
 - revised 	LinkedSockets <= 3 to compensate for removed redundant code 
 
# 0903 # HIGHLIGHT LEVELING LINKED GEAR
 - removed redundant code:
Show
	LinkedSockets >= 4
	ItemLevel <= 66
	Rarity Magic
	SetFontSize 36
	SetTextColor 100 100 255
	SetBorderColor 100 100 100
 - revised 	Rarity <= Magic to compensate for removed code

 - removed reduntant code:
Show
	Class "Gloves" "Boots" "Helmets" "Shields"
	LinkedSockets >= 3
	ItemLevel <= 25
	Rarity Magic
	SetFontSize 36
	SetTextColor 100 100 255
	SetBorderColor 100 100 100
 - revised 	Rarity <= Magic to compensate for removed code	

# 0904 # LEVELING WHITE/MAGIC ITEM PROGRESSION
 - removed explicit declaration of inherited property value (color) - (SetBorderColor 0 0 0)

# 0905 # LEVELING GENERAL RULES
 - removed explicit declaration of inherited property value (color) - (SetBorderColor 0 0 0)
 
# 5000 # TEMP AND WIP ENTRIES

# 5001 # WARBAND MODS - DEACTIVATED
 - removed
# OMEGA # ADDITIONAL RULES - ADD YOUR OWN RULES THAT WON'T OVERRIDE THE OTHER RULES

# XXXX # HIDE THE REST THEN FAILSAFE DISPLAY
 - font size change - (SetFontSize 23) SetFontSize 20
 - font size change - (SetFontSize 20) SetFontSize 19
 - font size change - (SetFontSize 45) SetFontSize 44
#
#---------------------------------------------------------------------------------------------------------------
# BEGIN NEVERSINK'S ORIGINAL COMMENTS
#---------------------------------------------------------------------------------------------------------------
# You can always find the latest version here:
#	http://pastebin.com/Af00CbhA
# Forum discussion thread. You can post question and feedback here:
#	http://www.pathofexile.com/forum/view-thread/1246208/page/1
# Please use this thread for feedback, questions and suggestions
#
#---------------------------------------------------------------------------------------------------------------
# INSTALLATION:
#---------------------------------------------------------------------------------------------------------------
#
# 1) Select-All + Copy this script from the "RAW Paste Data" at the bottom of the page.
# 2) Paste the contents into a notepad/txt document anywhere on your PC
# USE ANSI ENCODING IF YOU USE NOTEPAD++ OR ANY OTHER TEXT EDITOR
# 3) Click File/Save As and select the following settings:
# SAVE AS TYPE:	Select "All Files"
# FILE NAME:	"NeverSink.filter" (Without the ")
# SAVE LOCATION:	C:/Users/Documents/My Games/Path of Exile
# ENCODING (if available):	ANSI
# INGAME: Escape -> Options -> UI -> Scroll down -> Select NeverSink.filter
#
# IF YOU CAN'T SEE THE FILTER, YOU EITHER SAVED THE FILE IN THE WRONG FOLDER OR FAILED TO GIVE IT THE .filter FILE TYPE!
# IF YOUR ITEMS DISAPPEAR AFTER A WHILE CLICK "Z"
# IF YOU CAN'T PICK UP ANY ITEMS, YOU LIKELY CHANGED THE "item select key" WHILE SCROLLING DOWN
#
#---------------------------------------------------------------------------------------------------------------
# If you want to learn more about the syntax of item filters:
# http://pathofexile.gamepedia.com/Item_filter_guide
#---------------------------------------------------------------------------------------------------------------
# DESIGN GOALS:
#---------------------------------------------------------------------------------------------------------------
# - This setup is designed to assist players during all stages of path of exile gameplay (Leveling AND Endgame).
# - Highlight and notify players when worthwhile items drop
# - Use intuitive colors, without breaking the PoE feeling and immersion much. Don't go overboard on colors!
# - Provide light, scaling filtering during levelling
# - Provide comprehensive and in-depth filtering during endgame play
# - Provide evaluation help for high level rares based on criteria such as droplevel, itemlevel, item size, popularity and type. Helps you prioritize your pickups, while still showing everything!
# - Highlight recipe material (Regal, Chromatics, Glassblowers, Jewelers) and crafting bases
# - Easy to use setup
#---------------------------------------------------------------------------------------------------------------
#COLORS:
#Most colors remain the same, I want the filter to be very intuitive
#However, some improvements are implemented to improve your general efficiency
#1) Grey background items are usually vendor recipe material, such as:
#Chrom-Recipe, 6S, Chisel Recipe, Bauble Recipe.
#2) Starting with ilvl 65 rares will be split into 4 categories:
# Good (green BG), OK (regular BG), Bad (red BG) and excellent (green BG+green Border)
# Good rares are high tier bases, less clunky and usually worth checking
# Regular rares might end up being quite good, but usually are too clunky/average to be sellable
# Bad rares are low level bases that are usually pretty horrible and are only displayed for alt/alch shard purposes
# Excellent rares are rare rings/belts/amulets and jewels
#3) In addition 75+ rares will have a darker textcolor in order to display their viability for the regal recipe
#4) Orange border items are crafting materials - assorted 75+ items (mostly jewelry).
#5) Strong large orange border items are assorted 83-84 items suitable for endgame crafting
#6) Green border items are chancing bases.
#7) Higher tier currency has a different appearance to improve drop detection/priorization.
#8) Top tier items have a very distinctive appearance (opaqua white background with a strong color-border/text + large size)
#You usually will find those items every 10++ hours of endgame gameplay. Don't worry it won't clutter your screen
#9) Divination cards have a different appearance. (purple/pink themed)
#10) Maps, currency, uniues and divination cards have tier lists - better items will be larger/brighter
#---------------------------------------------------------------------------------------------------------------
# LOOKUP AND QUICKJUMP TABLE
#---------------------------------------------------------------------------------------------------------------
# Select one of the strings below and use the search function
# To jump to the section in the document
# (also use Notepad++ as a edit tool if you're not using it already)
#
# ALPHA # GLOBAL OVERRIDE - ADD YOUR OWN RULES THAT WILL OVERRIDE THE OTHERS HERE
# ALPHA-a # Talisman league!
# 0000 # UTILITY AND JUST-IN-CASE
# 0001 # LABYRINTH MATERIAL
# 0100 # TOP TIER RARITY
# 0200 # UNIQUES AND MAPS
# 0201 # UNIQUE TIER LIST
# 0202 # MAP TIER LIST
# 0203 # MAP FRAGMENTS
# 0300 # CURRENCY
# 0301 # TOP TIER: DIVINE, EXALTED
# 0302 # HIGH TIER: FROM ALCHEMY TO REGAL
# 0303 # MEDIUM-LOW ORBS
# 0304 # BOTTOM TIER: LOW ORB VARIATIONS
# 0305 # DIVINATION CARD TIER LIST
# 0306 # SPECIAL CURRENCY
# 0307 # REST
# 0400 # SOCKET/LINK BASED stuff
# 0500 # SKILL GEMS
# 0600 # RARE ITEM HIGHLIGHTING
# 060a # RARES SUITABLE FOR ENDGAME CRAFTING
# 060b # RARE RINGS, AMULETS, JEWELS, BELTS
# 060c # DROP LEVEL 69+ ITEMS ARE ALWAYS PRIORITIZED RARES
# 0601 # RARE DAGGERS
# 0602 # RARE CLAWS
# 0603 # RARE WANDS
# 0604 # RARE SWORDS
# 0605 # RARE AXES&MACES (1H)
# 0606 # RARE SCEPTRES
# 0607 # RARE STAVES
# 0608 # RARE TWO HAND SWORDS + MACES + AXES
# 0609 # RARE BOWS
# 0610 # RARE QUIVERS
# 0611 # RARE GLOVES, HELMETS, BOOTS
# 0612 # RARE SHIELDS
# 0613 # RARE BODY ARMOR
# 0614 # RARES - LEVELING SPECIFIC RULES
# 0615 # RARES - REMAINING RULES
# 0700 # NORMAL AND MAGIC ITEM RULES
# 0701 # 83+ ITEM CRAFTING
# 0702 # CHROMATIC ORB RECIPE ITEMS
# 0703 # CHANCE ORB BASES - ADD YOUR ITEMS HERE
# 0704 # HIGH LEVEL WHITE RINGS/AMULETS FOR ALCHING
# 0705 # MAGIC RINGS, AMULETS, BELTS
# 0706 # MAGIC JEWELS
# 0707 # CHISEL RECIPE ITEMS
# 0708 # HIGH LEVEL 4+ LINKED ITEMS
# 0709 # TOP BASES FOR CRAFTING
# 0710 # MARAKETH WEAPONS
# 0711 # PRE-ENDGAME 20% QUALITY ITEMS
# 0712 # ANIMATE WEAPON SCRIPT (DISABLED)
# 0800 # FLASKS
# 0801 # HIDE OUTDATED FLASKS
# 0802 # HIDE NON-QUALITY RANDOM FLASK DROPS IN MAPS
# 0803 # FLASKS - Hybrid Flasks (Normal)
# 0804 # FLASKS - Hybrid Flasks (Magic)
# 0805 # FLASKS - HIGHLIGHT NEW NORMAL FLASKS (Kudos to Antnee)
# 0806 # FLASKS - HIGHLIGHT NEW MAGIC FLASKS (Kudos to Antnee)
# 0807 # SHOW WHATEVER FLASKS REMAIN
# 0900 # LEVELING
# 0901 # LEVELING HIGHLIGHT JEWELRY
# 0902 # HIGHLIGHT LEVELING SPECIFIC ITEMS
# 0903 # HIGHLIGHT LEVELING LINKED GEAR
# 0904 # LEVELING WHITE/MAGIC ITEM PROGRESSION
# 0905 # LEVELING GENERAL RULES
# 5000 # TEMP AND WIP ENTRIES
# 5001 # WARBAND MODS - DEACTIVATED
# OMEGA # ADDITIONAL RULES - ADD YOUR OWN RULES THAT WON'T OVERRIDE THE OTHER RULES
# XXXX # HIDE THE REST THEN FAILSAFE DISPLAY
#
#---------------------------------------------------------------------------------------------------------------
# STYLE DATA FOR EASY SEARCH AND REPLACE
#---------------------------------------------------------------------------------------------------------------
#
###GENERIC BORDER###
#	SetBorderColor 0 0 0
#
###TALISMAN STYLE###
#	SetBorderColor 109 200 130 255
#
###TOP RARITY STYLE###
#	SetBackgroundColor 255 255 255 255
#
###MEDIUM RARITY UNIQUE BG###
#	SetBackgroundColor 175 96 37 255
#
###HIGH CURRENCY STYLE###
#	SetBackgroundColor 213 159 15
#
###MEDIUM CURRENCY STYLE###
#	SetTextColor 190 178 135 255
#
###DIVINATION CARD TIERS###
#	T1:	SetTextColor 255 0 175
#	T2:	SetBackgroundColor 235 15 200
#	T3: SetBackgroundColor 220 35 225
#	T4:	SetBackgroundColor 200 50 250
#	T5:	SetBackgroundColor 190 65 255
#
###83/84 CRAFTING BORDER###
#	SetBorderColor 255 255 0 255
#
###REGAL RECIPE RARE INDICATOR###
#	SetTextColor 255 190 0
#
###EXCEPTIONAL RARE INDICATOR###
#	SetBorderColor 25 180 25
#
###GOOD RARE INDICATOR###
#	SetBorderColor 30 90 45 230
#
###BAD RARE INDICATOR###
#	SetBackgroundColor 120 20 20 150
#
###UTILITY/VENDOR INDICATOR###
#	SetBackgroundColor 75 75 75
#
###ALCHEMY/LOWCRAFT INDICATOR###
#	SetBorderColor 255 190 0 150
#
###LOW SIZE CHROM RECIPE INDICATOR###
#	SetBorderColor 100 100 100
#
###MAGIC JEWEL BACKGROUND
#	SetBorderColor 0 150 200
#
###CHANCE ORB ITEM INDICATOR###
#	SetBorderColor 0 150 0 150
#
###ANIMATE WEAPON MODE###
#	SetTextColor 150 0 0
#	SetBorderColor 150 0 0
#
###PRIORITY MAGIC ITEMS (leveling+flasks)###
#	SetTextColor 100 100 255
#
###HIDDEN ITEMS: normal
#	SetBackgroundColor 0 0 0 100
#
###HIDDEN ITEMS: rare
#	SetBackgroundColor 0 0 0 150
#
#---------------------------------------------------------------------------------------------------------------
# SOUND DATA FOR EASY SEARCH AND REPLACE
#---------------------------------------------------------------------------------------------------------------
# Some new entries are not yet added to the list!
#
#The filter only uses 3 sounds:
#
#PlayAlertSound 6 300	high tier drops (all uniques, high orbs/cards/5-6links, high currency, fishing rods, 20% gems...)
#PlayAlertSound 1 300	medium tier drops (divination cards, orbs from alch to gcps)
#PlayAlertSound 4 300	map drops
#
#You'll quickly learn the 3 sounds while playing and will be able to recognize offscreen drops!
#---------------------------------------------------------------------------------------------------------------
# THANKS TO:
#---------------------------------------------------------------------------------------------------------------
# SCRIPT by NeverSink ( the-dude- on reddit )
#
# COMMUNITY:
# Special highlight for my Streamviewers, Redditors and Forum Pals
#
# DEVELOPERS:
# GGG - Thanks for the awesome game!
# "GGG_Bex" - Special thanks for providing information to keep the filter running well on league starts!
#
# FRIENDS:
# "c4pture" - Thanks for all the advise, help and for the fact that you're annoying only 75% of the time
# "Haggis & Tobnac" - Thanks for being good pals and POE-Teammembers
# "Malchron" - for helping out with his advice. And stuff.
#
# SUGGESTIONS / HELP:
# "Helmannn" - for helping to test the filter during the Ascendancy Alpha!
# "Antnee" - adapted some of his ideas. Also helped with feedback. He also has a nice lootfilter himself, check it out.
# "Ghudda" - I took his script as a template. It made learning the syntax even easier.
# "StarRune" - Found several flaws and improvement possibilities. Thanks!
# Also thanks to http://bschug.github.io/poedit/poedit.html - I used this site to test my setup
