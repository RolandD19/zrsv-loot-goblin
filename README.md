# ZERO Sievert tables and guides (zsrv-loot-goblin)

The tables below should help the loot-goblin-min-max player (for money and XP). Here, I focus on value per inventory cell rather than weight because you can drop loot anywhere (see tips below on dropping loot by extract).
- _This is just an informational wiki (no mods) and based off the vanilla game._
- _All the tables' info were taken from the game's JSON files._
- Money is typically more of a concern for those playing on Hunter difficulty, less so for non-hardcore difficulties.

## Item tables (with values per Inventory cell)

<!-- grusa:63000+15000+15000+8500+7200+12000 -->

- [Loot items](docs/bimr.md) - Various loot items, sorted value value per cell (not in tables below)
- [Weapons](docs/weapon.cell.md) - Sorted by value per cell
- [Armor](docs/armor.md) - Sorted by value
- [Ammo](docs/ammo.md) - Sorted by full stack value
- [Grenades](docs/grenade.md) - Sorted by full stack value
- [Attachments/mods](docs/mod.md) - Sorted by full value
- Backpacks - Excluded because they oddly have an additional sell penalty (divide by 5), so the per-cell value of the best packpack found in raid (CC-03 worth 60000) is only 3000.
- [All tables](docs/all-tables.md) - All tables on one page (each table collapsible)
- As you can see from the tables, compared to other items one can find in raid, most early/mid-game weapons are not worth taking back from raid (even with mods and later repairing to 100%), if your goal is to sell them.
  - A Grusa 4 has relatively high value per inventory cell, as the weapon takes up 6 cells. A fully-decked Grusa 4 with Vadoo scope and modern torch will be worth ~20K rubles per inventory cell (which is actually decent, but fully decked weapons are rare to find). A more modestly-decked Grusa 4 (with Spec scope+regular torch) is worth ~15K per cell, assuming 100% durability.
- Higher tier armors (when repaired to 100%) and armor-piercing (BP/AP) ammo (full stacks) tend to offer the most value per inventory cell.
- During mid/end-game, the items that a loot goblin takes back to sell should be worth at least 10K rubles per inventory cell. From a long raid, I find myself often gathering full stacks of 7.62x39 BP and 5.56x45 M995 (BP) ammo, each worth 30000 and 25500 respectively.
- Because grenades now stack (v1.3.0+), a full stack now offers high value.

## Tips for the loot goblin

- You can **drop off loot anywhere/anytime** in a raid - rather than lugging everything around. This way, you'll minimize your stamina loss. Press Tab and you'll notice the right pane says "Ground". Moving items there will result in a box on the ground.
  - I drop multiple items throughout a raid, mark them on the map, and come back to them later.
  - For example, before entering the Makeshift camp's laboratory, drop everything you don't need by the entrance.
  - Create these boxes in a "safe" area (somewhere with cover), so you're a bit more protected from wandering NPCs/mobs.
- Do this at the border of the **extract zone**. You can create multiple boxes right on top of one another. Then - when you're ready to leave - move unencumbered into the extract zone (i.e. just on the otherside of the boxes) and pick/choose what you want. Make sure to watch the extract timer if you're not in Inventory and press Tab (to reset the timer) if you're not ready to leave.
  - If you have the Mule hunter perk, then you can just walk slowly into extract rather than selecting your items from within the zone.
  - You can do all this within the extract zone, but then you'll have to mind the timer more often.
  - One extract zone per raid will usually have some kind of **extract camper**, usually a hunter but sometimes mobs.
- If you're going to scrap weapons, remember to take the attachments/ammo off, as those do not contribute the weapon scrap you get.
- If you intend on crafting bunker/hideout modules, collect and save rare items early: bolt cutters, car batteries, propane tanks, military circuits, etc.

## XP and other min/maxing

- [NPC/mob table](docs/npc.md) - Maximize XP with minimal bullets!
- You can **switch out** your bunker modules now. In my current run, I've made all the modules (except Garden and Lights kit) to their max levels. When I leave for a raid, I switch out my Ammo Producer, Scavenger, and Workshop for Shooting Range, Infirmary, and Gym (as those give in-raid buffs). When I return, I put the first three back in, and collect the materials from Ammo Producer and Scavenger. Materials-giving modules seem to reset like the bunker traders (7AM). I leave in Forge so I can scrap if needed during the raid.
- As for scrapping weapons and armor, the amount of material produced is proportional to the item's value multiplied by its durability. 

<details>
<summary>More on XP with slight spoilers</summary>

I haven't done the math but - because of the **high XP from rotfangs** - I think clearing the Swamp map's sewer will give about as much XP as clearing the Makeshift Camp's laboratory (even including the second lab area that has multiple infestations), and clearing that sewer is much easier and less time-consuming than clearing the labs. Rotfangs' XP gain is unbalanced for now, so take advantage while you can!

</details>

## More (or your own) radio music

There are 20 music tracks packaged with ZERO Sievert; one extra OGG file appears unused. Currently, the following 8 tracks are unlocked by default:

id | filename | track name
:--|:--|:--
theloners_colours | snd_radio_TheLoners_Colours.ogg | colours
theloners_fireplacefolk | snd_radio_TheLoners_FireplaceFolk.ogg | fireplace_folk
theloners_lazysunday | snd_radio_TheLoners_LazySunday.ogg | lazy_sunday
main_menu_1 | snd_radio_main_menu_1.ogg | hunters_guitar_track
main_menu_2 | snd_radio_main_menu_2.ogg | zero_sievert_ost
igor_appletree | snd_radio_Igor_AppleTree.ogg | apple_tree
igor_lovelyday | snd_radio_Igor_LovelyDay.ogg | lovely_day
igor_windowglance | snd_radio_Igor_WindowGlance.ogg | window_glance

The cassette in the forest bunker has the following track (which you can add to the radio):

id | filename | track name
:--|:--|:--
kyle_campfire_guitar | snd_radio_kyle_campfire_guitar.ogg | my_home_the_zone

At the moment, the only way to access the remaining tracks is to either add them to your save file (`save_shared_[123].dat`) or more simply, unlock them in the `radio_music.json` file, which resides two subfolders under the game's root folder, e.g., `Program Files (x86)/Steam/steamapps/common/ZERO Sievert/ZS_vanilla/gamedata`.
- To unlock the rest, just open `radio_music.json` in Notepad, and find/replace all instances of `false` to `true`.

If you want to listen to **your own** OGG tracks:
1. Just overwrite one of the OGG files that your player's save has access to. If you unlock all tracks, then just overwrite any one of the the audio files. All the OGG files are the game's root folder, e.g., `Program Files (x86)/Steam/steamapps/common/ZERO Sievert`.
2. If you instead want to be able to play _all_ the original audio files and add your own. Wellll, that's a bit more involved. Monkeying with the JSON game files isn't enough. The main game file `data.win` needs to know about the OGG audio file (hard-coded).

For that, you need [UTMT (UnderTaleModTool)](https://github.com/UnderminersTeam/UndertaleModTool):
1. First make a backup of the `data.win` file.
2. Open the `data.win` file in UTMT.
3. For convenience: In the upper left search filter field, type in `snd_radio`.
4. Open the Sounds entry. You'll see only the music/radio resources.
5. Double click on one of the entries (as a template for your new sound resource).
6. Then, right click on the Sound line itself and click on Add (it's the only available action).
7. Give it a name following the same format, e.g., `snd_radio_U2_WithorWithoutYou` .
8. Set the non-name fields/checkboxes to match the template you opened up in step #5.
    1. For "File", best to keep same as "Name", but append `.ogg`, e.g., `snd_radio_U2_JoshuaTree`.
    2. For "Audio group", you'll need to clear that upper left search bar (where you presumably typed in "snd\_radio" and then open up the "Audio groups". From there, you can drag the "audiogroup\_default" into your new entry.
9. Make sure to save the `data.win` file!
10. Next, you'll need to add the new entry into `radio_music.json` file. You can do so in Notepad. 
    - I recommend adding your new entry near the end, after the `"theloners_trainstation"` entry. Just make a copy of it and make sure to end the previous entry with a comma.
    - The `name` and `artist` fields don't matter, but everything else needs to line up with what you did in `data.win`. Also, I recommend keeping the lower/uppercase conventions, in the names and ids.
	- If you set `"unlocked_by_default": true`, you won't need to monkey with the save file to have your player access the track.
	
Enjoy!

Here are the radio filenames that are locked by default:
filename|
:--|
snd_radio_Igor_MondayBlues.ogg  |
snd_radio_Igor_TheClassic.ogg |
snd_radio_Igor_TheSecret.ogg |
snd_radio_MrJunk_FunkyJunk.ogg | 
snd_radio_TheLoners_CountryRoads.ogg | 
snd_radio_TheLoners_ForestWalk.ogg | 
snd_radio_TheLoners_GuitarDance.ogg | 
snd_radio_TheLoners_MellowMorning.ogg | 
snd_radio_TheLoners_OldFriend.ogg | 
snd_radio_TheLoners_SpringTime.ogg | 
snd_radio_TheLoners_TrainStation.og |

## Other useful tables:

- [Difficulty settings](docs/difficulty.md) - Compare the difficulty settings; not yet updated for v1.3.0+
- [Gun mastery/skills table](docs/gun-skills.md) - Full description of all gun mastery skills, organized a bit differently than the wiki's [Gun Mastery](https://zero-sievert.fandom.com/wiki/Gun_Mastery) page.

## My other GitHub ZERO Sievert resources:

[Custom maps](https://github.com/RolandD19/zrsv-maps) -- Proof-of-concept for custom (AI-generated) maps

<!-- ## Prev test -->

<!-- Price | Item -->
<!-- :--|:-- -->
<!-- 3000 | Gun -->
