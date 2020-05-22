# War-of-the-Elements
Machine Project on Programming on Structured Data Types 



The game consists of 4 elements (Water, Earth, Fire, Air) and numerous characters (a minimum of 4 characters, and a minimum of 1 aligned to each element), each of which can either be assigned to be aligned with the Water element, Earth element, Fire element, or Air element.

The project will require the implementation of two modes: Gameplay Mode and Configure Mode.

Gameplay Mode

At the start of the game mode, the user has the option to select either the “Free mode” or the “Storyline mode”.
•	Free mode: Player may select their own character and select their opponent through the character select screen. The battle follows normal rules and the player is returned to the character select screen after the conclusion of the battle
•	Storyline mode: The player may select their own character, but their sequence of opponents is predetermined through a specific story that will be selected by the user (See Configuration mode, storyline module) ***. When the player defeats an opponent, they proceed to the next opponent, until they finish the last stage. If, during a battle the player is defeated, the game is over and they are sent back to the main menu.
*** A character with no storyline associated to them cannot be selected in Storyline mode
The Game mechanics

The game will follow a turn-based sequence. This means that both players will not move at the same time, rather the player will make their move (charge / damage the opponent) and only upon the conclusion of their turn will the opponent make their move. The sequence will repeat until one of the characters is considered victorious.

At the start of the round, the first player is determined randomly and the battlefield should be displayed to the user.

The battle field will display the following during:
•	The name of the player’s character and opponent respectively
•	The elemental affinities of both characters
•	The available hitpoints (HP) of both characters
•	The available power (PP) of both characters
•	The player’s available moves (During the player’s turn)
•	Stage number (If in storyline mode) and Stage name (attributed to the opponent)
Stage:  1
“Sea of Olympus”

     Theriel the Wise                                         Poseidon       
        “Air”                     vs                         “Water”
   HP:    350 / 350                                   HP:    500 / 500
   PP:      0 / 20                                    PP:      0 / 35

Player’s Turn!
Select Move:
[1] Charge – Gain 3 points of PP
[2] Aerial blast – Attack with the force of the wind (Required PP: 3)
[3] Wind of Fury – Summon the atmosphere’s combined powers to attack (Required PP: 9)
[4] Gale abyss – Unleash the wrath of the heavens upon the opponent (Required PP: 15)


Rules:

1.) At the start of the game, both players will have 0 PP. PP is required to perform certain moves.
2.) At the player’s turn:
- The player may have the option to use any of the moves they have available, provided that they have enough PP to perform it. The option for moves to be made is as follows:
- Charge: A default move set available for all characters regardless of their affinity or their stats. This allows them to gain 3 PP. Doing this automatically ends the turn.
- Light attack: Performs an action that consumes 10 – 20% of the maximum PP. This attack deals 5 – 15% of the player’s maximum HP, but it has a 25% chance of missing and dealing 0 damage.
- Medium attack: Performs an action that consumes 30 – 50% of the maximum PP. This attack deals 20 – 30% of the player’s maximum HP, but it has a 10% chance of missing and dealing 0 damage.
- Heavy attack: Performs an action that consumes 60 – 80% of the maximum PP. This attack deals 40 – 50% of the player’s maximum HP and has a 0% chance of missing.
- Damage dealt to the opponent and move used should be displayed to the user.
- At the end of the turn, if the player did not use “Charge”, they will gain 2 PP automatically. Note that the value of PP will never exceed the player’s maximum PP.


3.) At the opponent’s turn:
- The opponent may have the option to use any of the moves it may choose, with a  40% chance of using “Charge” and a 60% chance of doing any of the moves available given the PP is currently has. Note that is cannot perform moves that require more PP than it currently has. (The cost is similar to that of the player’s: 10 – 20% of the maximum PP, 30 – 50% of the maximum PP, 60 – 80% of the maximum PP)
- Damage dealt to the player and move used should be displayed to the user.
- At the end of the opponent’s turn, if the opponent did not use “Charge”, they gain 2 PP automatically.

NOTE: The cost of PP needed to perform certain moves will be determined at the start of the battle and will remain the same for the battle’s duration, but they will always fall within the designated ranges specified.

Taking Damage

Anyone who takes damage loses that amount on their HP. A character is considered defeated if their respective HP reaches 0.
Elemental affinities are considered in taking damage. If a character’s elemental affinity is considered weak against their opponent’s, then that character will take 1.5x the amount of damage dealt by the opponent. See the following table for weaknesses.

Element	Weakness
Water	Earth
Earth	Air
Air	Fire
Fire	Water

Elemental affinities battling their own element will receive only 75% of the damage dealt to them.

Configure Mode

In configure mode, the user is able to modify the characters by adding, modifying, or deleting characters, and modifying their move sets. The user is able to modify the characters and their storyline configurations as well as their elemental affinities and stats.

There are 3 modules available and selectable by the user, namely the Character module, the storyline module, and the moves module. They are as follows:

Character module (*)
1.) Add Character – The user is able to add a new character by giving it a name, location name (stage name when the respective character is the opponent), assigning it an elemental affinity, specifying the maximum HP and the maximum PP. New characters will have a blank move set and cannot be selected unless their move set is complete. (See the move set module)
2.) Modify Character – The user is able to modify the character’s name and elemental affinity as well as their respective maximum HP and maximum PP.
3.) View Character – The user is able to view a list of characters created. The user should also have the option to view characters by elemental affinity.
4.) Delete Character – The user is able to select a character and delete them. If the character has a storyline associated to them, the storyline is also deleted. **
(* There has to be a minimum of 4 characters, with 1 character present for each element. If the condition is not met, an error message should occur and the user should not be allowed to leave the module until they have created enough characters)
(** If the deleted character is an opponent of another character’s storyline, they are replaced by a random character in that storyline)
Move set module
1.) Add a move – The user is able to add a move. A move has a name, a description, a classification as a light attack, medium attack, or a heavy attack, and an elemental affinity.
2.) Modify move – The user is able to modify the move’s name, description, classification, and elemental affinity.
3.) View move – The user is able to view a list of moves available. The user should have the option to view moves by category, elemental affinity, or both.
4.) Delete move – The user is able to select a move and delete them. If the move has been associated to a character, that move is replaced by a random one.
5.) Set moves – The user is able to assign particular moves to the characters. Note that a character can only be assigned that move if the character’s and the move’s elemental affinity matches each other. 

Storyline module:
1.) Add a story – The user is able to add a story. A story has a title, the protagonist (Player character), a description, and a set of opponents. The ideal number of opponents in the storyline setting is 3, but the user has the ability to change the number of opponents they will face (minimum of 3, and no opponent should be allowed to be selected more than once. The protagonist cannot also battle themselves)
3.) Modify Story – The user is able to modify the set of opponents a character will battle in Storyline mode as well as the title, protagonist and description
3.) View story – The user is able to view all available stories created. The user should be able to view stories by character / protagonist
4.) Delete story – The user is able to select a story and delete it.
