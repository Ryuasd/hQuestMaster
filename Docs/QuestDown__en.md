# QuestDown Documentation v0.1


## General Event Syntax

An event starts with a block {\[\[(marker), event1, event2, ...\]\] text or actions}. The marker represents the position on the map to which the event is associated and can be either "Arrow" or a letter from A to Z or a number from 1 to 9. After the marker, one or more events are listed separated by commas.

Note: If a marker is not present on the map, this event will never be triggered.

Following the event, either a text (which will be immediately shown to the player as communications) or an action must be specified. It is possible to concatenate multiple actions and texts. When it is necessary to indicate a specific cell with an action or event, it should be represented by a combination of a letter (from A to S) and a number from 1 to 26. You can view the coordinates of a cell directly from hQuestBuilder by holding down Q and D together, which will display a small box in the bottom right corner of the browser containing the coordinates of the selected cell.

Any other text outside {} will be ignored, so you can leave the original notes of the maps.

## Supported Events

•	**START**: Not an actual event but indicates that the heroes will start the game at the marker's position.

*Example:*

    {[[(X), START]]}

•	**ON\_SEARCH\_TREASURE**: Triggered when a hero performs a treasure search.

If the marker is in a Room, it is executed when a search is performed in that room. If it is in a Corridor, it is executed when a search is performed, and the marker is in line of sight with the searching hero.

*Example:*

    {[[(A), ON_SEARCH_TREASURE]] You found a Key!}

•	**ON\_ENTER\_ROOM**: Triggered when a hero enters the room where the marker is present.

Normally, it is only activated the first time one of the heroes enters the room. If the :REPEAT option is specified, the event will be activated each time a hero enters the room.

*Example:*

    {[[(F), ON_ENTER_ROOM]] You see a wrecked table!}

*Example*:

    {[[(F), ON_ENTER_ROOM:REPEAT]] You hear a strange noise coming from the south wall..}

•	**ON\_SHOW**: Triggered when the cell where the marker is located becomes visible (in line of sight with a hero).

*Example:*

    {[[(A), ON_SHOW]] You find a patrolling orc!}

•	**ON\_OPEN**: Triggered when a hero opens a door or secret door at the marker's position.

*Example:*

    {[[(H), ON_OPEN]] The door is rusty, and you have to use force to open it.}

•	**MONSTER\_ON**: Used to specify details of a monster already placed on the map.

First, place a monster in a cell, for example, a Goblin in cell B12, and then use MONSTER\_ON to specify all the monster's attributes on cell B12.

Attributes are optional and include:

•	NAME: The monster's proper name.•	MOV: The number of cells it can move each turn.•	ATK: The monster's attack value.•	DEF: The monster's defense value.•	BODY: The monster's health points.•	MIND: The monster's mind points.•	TYPE: Currently, the only acceptable value is PASSIVE, indicating that the monster is passive and will not attack the heroes. If omitted, the monster will use normal AI behavior.

*Parameters*:  \[cell\_name, NAME=monster\_name, MOV=movement, ATK=attack, DEF=defense, BODY=health\_points, MIND=mind\_points, TYPE=type\]

*Example:*

    {[[(M), MONSTER_ON(B12, NAME=Greep, MOV=1, ATK=1, DEF=1, BODY=1, MIND=2, TYPE=PASSIVE)]]}

•	**ON\_STEP**: Triggered when a hero takes a step into the specified cell.

*Example:*

    {[[(J), ON_STEP]] The floor seems unstable..}

•	**ON\_TRAP\_TRIGGER**: Triggered when a trap is activated in the specified cell.

*Parameters*: \[cell\_name\]

*Example:*

    {[[(I), ON_TRAP_TRIGGER(G16), ON_TRAP_TRIGGER(L10)]] This chest is a trap! Roll 2 x battle dice and lose 1 HP for each skull rolled}

•	**ON\_DEATH**: Triggered when a monster (originally placed in the specified cell) dies.

If multiple cells are indicated, it is only triggered when all those monsters are dead.

*Parameters*: \[cell\_name1, cell\_name2, ...\]

*Example:*

    {[[(Q), ON_DEATH(J12, J15)]] You've killed your targets; now you can escape to the stairs!}

## Supported Actions

Actions are indicated with the syntax \[\[action\]\]. Some actions may require specific parameters.

•	**\[\[ASK: question\]\] … \[\[ELSE\]\] … \[\[END\]\]**: Displays a question to the user and waits for an answer.

If an affirmative answer is given, the subsequent text is shown and/or the actions present until the \[\[ELSE\]\] or \[\[END\]\] block are executed. In the case of a negative answer, the subsequent text is shown and/or the actions between the \[\[ELSE\]\] and \[\[END\]\] blocks are executed.

The \[\[ELSE\]\] block is optional.

*Example:*

\[\[ASK: Do the heroes want to put their hand into a mysterious bag?\]\] You found a gem! \[\[END\]\]

*Example:*

    [[ASK: Do you have the key?]] [[OPEN(S23)]] [[ELSE]] [[LOCKED]] [[END]]

•	**\[\[OPEN\]\]**: Opens a door or secret door at the marker's position.

*Example*:

    [[OPEN]]

•	**\[\[OPEN(cell\_name)\]\]**: Opens a door or secret door in the specified cell.

*Parameters*: (cell\_name)

*Example:*

    [[OPEN(G11)]]

•	**\[\[LOCKED\]\]**: Indicates that a door or secret door is locked and cannot be opened.

*Example*:

    [[LOCKED]]

•	**\[\[LOCKED: message\]\]**: Indicates that a door or secret door is locked and displays a message to the user.

*Example*:

    [[LOCKED: This door is locked by magic!]]

•	**\[\[REMOVE(cell\_name)\]\]**: Removes an element from the specified cell.

*Parameters*: (cell\_name)

*Example*:

    [[REMOVE(R14)]]

•	**\[\[ADD\_NPC(cell\_name, attributes)\]\]**: Adds a non-player character (NPC) to the specified cell.

Attributes are required and include:

•	NAME: The NPC's proper name.•	MOV: The number of cells it can move each turn.•	ATK: The NPC's attack value.•	DEF: The NPC's defense value.•	BODY: The NPC's health points.•	MIND: The NPC's mind points.•	ON\_DEATH (optional): The event to trigger in case of NPC death. Any event or message can be specified.

*Parameters*: (cell\_name, ATTRIBUTES)

*Example*:

    [[ADD_NPC(K12, NAME=Prince Bart, MOV=1, ATK=0, DEF=0, BODY=2, MIND=2, ON_DEATH=[[QUEST_FAILED]])]]

•	**\[\[QUEST\_OBJECTIVE\_COMPLETED\]\]**: Indicates that a quest objective has been completed.

Upon completion of the quest, it will be evaluated as completed or not.

*Example*:

    [[QUEST_OBJECTIVE_COMPLETED]]

•	**\[\[QUEST\_COMPLETE\]\]**: Indicates that the quest has been completed.

If this tag is absent, the quest will autonomously end when all heroes reach the stairs.

*Example*:

    [[QUEST_COMPLETE]]

•	\[\[QUEST\_FAILED\]\]: Indicates that the quest has failed.

*Example*:

    [[QUEST_FAILED]]

&#x200B;

This is a comprehensive overview of the events and actions supported by the QuestDown language. Use this documentation as a reference while developing your interactive maps for hQuestMaster.

&#x200B;

**For new kinds of Automations needed (and so new QuestDown Events/Actions) please open a new post with flair "Feature Request"!**
