<h2>Changelog v0.180</h2>01/12/2023<br>
<ul class="news">
    <li>[FEATURE] Lots of improvements on ON_SERACH_* Events, and other events.</li>
    <li>[FEATURE] Support for multiple events for single Mark.</li>
    <li>[FEATURE] Added support for Repeated trigger for many events, with optional parameter :REPEAT or :R</li>
    <li>[FIX] Various bug fix and improvments (thank you Agorg for the reports!)</li>
</ul><br>13/10/2023<br>
<ul class="news">
    <li>[FEATURE] Improved quest selection page, to show Introduction and Author of the quests.</li>
</ul><br>12/10/2023<br>
<ul class="news">
    <li>[FIX] Completely reworked QuestDown core system, to correctly mantain the execution order in case of multiple
        actions.
    </li>
    <li>[FIX] Reworked parser for IF and ASK to, to corretly manage annidiated IF and ASK.</li>
</ul><br>23/08/2023<br>
<ul class="news">
    <li>[FEATURE] Added new Option in the Settings to disable the alerts for place/'update position' of heroes,
        monsters, and objects.
    </li>
</ul><br>22/08/2023<br>
<ul class="news">
    <li>[FEATURE] Added new events ON_SEARCH_TRAP, ON_SEARCH_HIDDENDOOR, ON_END_FIRSTHERO_ ON_END_ALLHEROES,
        ON_SINGLE_HERO_DEATH, ON_ALL_HERO_DEATH.
    </li>
</ul><br>17/08/2023<br>
<ul class="news">
    <li>[FEATURE] Added buttons to "Kill" and "Bring back to Life" a Hero.</li>
    <li>[FEATURE] Small improvements in all system messages, adding colors for Hero and Monster Names.</li>
</ul><br>16/08/2023<br>
<ul class="news">
    <li>[FEATURE] Added support QuestDown syntax: Added Chaos/Terror Spells for Monsters defined with MONSTER_ON.</li>
</ul><br>11/08/2023<br>
<ul class="news">
    <li>[FEATURE] Added support QuestDown syntax in Wandering Monster field of hQuestBuilder.</li>
</ul><br>10/08/2023<br>
<ul class="news">
    <li>[FEATURE] Added support in QuestDown Syntax: for new action ADD_MONSTER, to do dynamically add a monster at a
        cell position.
    </li>
</ul><br>09/08/2023<br>
<ul class="news">
    <li>[FIX] If during a quest was added a NPC, it would disappear after a realod of the app.</li>
    <li>[FIX] The status applied by Spells was lost after a reload of the app.</li>
</ul><br>08/08/2023<br>
<ul class="news">
    <li>[FEATURE] Added support in QuestDown Syntax: for new action IF, to do conditional checkings.</li>
    <li>[FEATURE] Added support in QuestDown Syntax: for SET &amp; GET, to save information in Variables, and then use
        them with GET with the new IF action
    </li>
    <li>[FEATURE] Added support in QuestDown Syntax: for RND to generate a Random number to be used with IF.</li>
    <li>[FEATURE] Added support in QuestDown Syntax: for TURN to get the current turn count be used with IF.</li>
    <li>[FEATURE] Now in the "Zargon Turn" button, is also show the current turn number.</li>
    <li>[FEATURE] Added support in QuestDown Syntax: for new starting event HIDE_ON to hide an object (Furniture, Block,
        Door) at the beginning of the quest.
    </li>
    <li>[FEATURE] Added support in QuestDown Syntax: for new action HIDE to hide an object: Furniture, Block, Door.</li>
    <li>[FEATURE] Added support in QuestDown Syntax: for new action SHOW to show an hidden object: Furniture, Block,
        Door) hidden with HIDE_ON or HIDDEN.
    </li>
</ul><br>07/08/2023<br>
<ul class="news">
    <li>[FEATURE] Added support in QuestDown Syntax: for individual starting position for each Hero, with START().</li>
    <li>[FEATURE] Added support in QuestDown Syntax: for MOVE_HERO, MOVE_MONSTER and MOVE_OBJ to move respectly Heroes,
        Monsters and Furniture &amp; all Objects
    </li>
</ul><br>05/08/2023<br>
<ul class="news">
    <li>[FIX] A triggered Spear trap was not removed correctly after a reload of the map.</li>
    <li>[FIX] When 2 Doors (or Secret Doors) was on the same cell, you could open only one.</li>
    <li>[FIX] Genie spell in case of 2 Doors (or Secret Doors) on the same cell, was not working correctly.</li>
</ul><br>15/07/2023<br>
<ul class="news">
    <li>[FEATURE] Added button to toggle FullScreen mode.</li>
</ul><br>14/07/2023<br>
<ul class="news">
    <li>[FIX] Added a message to "Update monster position", when a monster move but cannot attack.</li>
    <li>[FEATURE] In the monster card, added the label "Damages".</li>
    <li>[FEATURE] Added pulsing red effect for dice rolled result "Skull"</li>
</ul><br>13/07/2023<br>
<ul class="news">
    <li>[FEATURE] Added step-count also on tiles when moving a Hero.</li>
    <li>[FEATURE] Forming a Party, now you can choose the style (EU, USA, HQ21) for the hero icon.</li>
</ul><br>12/07/2023<br>
<ul class="news">
    <li>[FIX] Rewritten movement to fix the case of "pass through another hero.</li>
    <li>[FIX] On any kind of Search, show alert if there are monsters in line of sight of the selected Hero.</li>
    <li>[FIX] All heroes are now allowed to search in one room, but only the first hero trigger the ON_SEARCH_TREASURE
        event.
    </li>
    <li>[FIX] Wandering monster, now attack in the same turn that come into play.</li>
</ul><br>10/07/2023<br>
<ul class="news">
    <li>[FEATURE] Now from Settings you can choose your preferred style (EU, USA, HQ21) for Tiles and Monsters</li>
</ul>