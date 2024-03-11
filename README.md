# hQuestMaster
hQuestMaster is an alternative (FREE) web app to the official app of HeroQuest, to play homebrew quest with an automated Zargon!

Link: https://www.hquestmaster.com

Being a Web App, theorically can run on any modern browser (Desktop, Tablet or Mobile) but later i will also release an ad-hoc App for Android and iOS.

At this time, only the base Game System is officially supported.
I'm working on implementing all the tiles & rules of all official expansions, and also for homebrew tiles!

<br/>

## Backstory
I wanted to play new quests created by the community but wihtout the need of a Zargon player, and with the possibility to use as many house rules i'd like.

To begin with i needed a tool to create the quests, i started working with Heroscribe maps but then after a good talking with the creator of hQuestBuilder (/u/squidgem0nster) i implemented import of HQB maps and developed a kind of language to create automations for the maps events (like when entering a room, or stepping on a tile, or killing a monster, ecc..) called QuestDown, that need to be written inside the Note of the quest.

Wrtiting with this syntax is possible the create automations for any Mark sign put in the map (like Arrow, Letters o Numbers); From defining a starting point, to events to be played when entering a room or on the death of a monster!
This system was a big improvment the one that i previosly used (additional xml definitions), because is more flexible ad adaptable for homebrew maps!
So i went for a full support of maps created with hQuestBuilder, and doing this, for now, the support of maps made HeroScribe (.xml) is broken (maps are loaded, but there is no support for automations at the moment), i will work on it later.

A little clarification, what i wanted to create was not a "videogame", so many things are left to the users. For example, BP of each heroes need to be tracked on your character sheet, or the fact that are present only the spells that need an interction with Zargon.
Everything that not strictly require a Zargon player is implemented, you allways be required to have a phisical copy of HeroQuest! 

<br/>

## How
Anyone can create their own quest and play it with hQuestMaster!

Here is some early documentation on how a quest should be written with the QuestDown language:

[QuestDown - Documentation (EN)](https://github.com/Ryuasd/hQuestMaster/blob/main/Docs/QuestDown%20-%20Documentation%20-%20v1.1.EN.pdf)

[QuestDown - Documentazione (IT)](https://github.com/Ryuasd/hQuestMaster/blob/main/Docs/QuestDown%20-%20Documentazione%20-%20%20v1.1.IT.pdf)


And in the [Quests folder](https://github.com/Ryuasd/hQuestMaster/tree/main/Quests) you can find the files .hqb of the quests actually included in hQuestMaster.

<br/>

## Help
For any question, problem, or suggestion, you can reach me with the Feedback button of the right site of site, or with this Google from:
https://docs.google.com/forms/d/1KzcPoeBs0RWi4bOEoBGXn4XXCfmsr1tztEV8FwwbRZY

Or you can find me:<br>
on [Facebook](https://www.facebook.com/hQuestMaster)<br>
on [Reddit](https://www.reddit.com/r/hQuestMaster/)<br>
on [Discussions](https://github.com/Ryuasd/hQuestMaster/discussions)

<br/>

## Thank you 
Thank you Milton Bradley, Games Workshop and Hasbro to have given us this great game! 
And a big thank you to all the community of HeroQuest, that makes this game always aswesome with their love and inspiration!

Special thanks goes to:<br>
<a target="_blank" href="https://www.reddit.com/user/squidgem0nster/">/u/Squidgem0nster</a> for his great tool <a target="_BLANK" href="https://www.hquestbuilder.com">hQuestBuilder</a>, and for his great support and help creating this project!<br>
<a target="_blank" href="https://www.reddit.com/user/Banjo-Oz">/u/Banjo-Oz</a> for supplying his great set of SVG Icons for Heroes/Monsters and all Furnitures!<br>
<a target="_blank" href="https://www.reddit.com/user/Agorg2202">/u/Agorg2203</a> for Beta Testing, suggested nice improvments, and also wrote the documentation of the QuestDown language!<br>
<a target="_blank" href="https://www.reddit.com/user/Aster28_/">/u/Aster28_</a> for Beta Testing, for his tool <a target="_BLANK" href="https://www.hquestmaster.com/QDT/QuestDownTranslator.html">QuestDown Translator</a>, and for his help to disclose and advertise QuestDown and hQuestMaster!
<br>
A big thanks also for all Beta Testers that helped me to test and improve hQuestMaster!

<br>

## Discalmer
hQuestMaster is an application developed, non-profit, by Ryuasd 2023. 

HeroQuest is a trademark of the Hasbro - Games Workshop Inc. - All rights reserved. 
This web app doesn't intend to injure in direct or indirect way copyrights to the ownership of the trademark.

<br/>

