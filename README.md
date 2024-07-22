

# UnitScan-Turtle (Hardcore Version)

## Description
This fork extends [unitscan-turtle](https://github.com/GryllsAddons/unitscan-turtle) by provinding a prepopulated list of  dangerous elite mobs, rares, and other units. This version is especially useful if you're playing Turtle WoW's hardcore mode.

## Preview
![Example1](preview/unitscan1.jpg)
![Example2](preview/unitscan2.jpg)
![Example3](preview/unitscan3.jpg)

![Example3](https://github-production-user-asset-6210df.s3.amazonaws.com/23161804/351084262-835e06ea-c42f-464c-b2fb-cb5800e48db0.mp4?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=AKIAVCODYLSA53PQK4ZA%2F20240722%2Fus-east-1%2Fs3%2Faws4_request&X-Amz-Date=20240722T191019Z&X-Amz-Expires=300&X-Amz-Signature=9586a67f0de6f193fa06b1551185c42dd39104038905306d3c989153ad521bb1&X-Amz-SignedHeaders=host&actor_id=23161804&key_id=0&repo_id=803506643)

![Example3](https://github.com/user-attachments/assets/835e06ea-c42f-464c-b2fb-cb5800e48db0)

![Example3](https://camo.githubusercontent.com/2ef44eebab46a7db995de3e7dadb488b42c12499c307201ef9c7ecb32bc0011c/68747470733a2f2f6769746875622d70726f64756374696f6e2d757365722d61737365742d3632313064662e73332e616d617a6f6e6177732e636f6d2f32333136313830342f3335313038343236322d38333565303665612d633432662d343634632d623266622d6362353830306534386462302e6d70343f582d416d7a2d416c676f726974686d3d415753342d484d41432d53484132353626582d416d7a2d43726564656e7469616c3d414b494156434f44594c5341353350514b345a41253246323032343037323225324675732d656173742d312532467333253246617773345f7265717565737426582d416d7a2d446174653d3230323430373232543139313031395a26582d416d7a2d457870697265733d33303026582d416d7a2d5369676e61747572653d3935383661363766306465366631393366613036623135353131383563343264643339313034303338393035333036643363393839313533616435323162623126582d416d7a2d5369676e6564486561646572733d686f7374266163746f725f69643d3233313631383034266b65795f69643d30267265706f5f69643d383033353036363433)



The list of units can be found in [zone targets.lua](https://raw.githubusercontent.com/RetroCro/unitscan-turtle/master/zonetargets.lua).


 - Unitscan will only look for zone targets specific to your current
   zone. The target list is reloaded when you change zones.
   
-   Zone targets will be reloaded 90 seconds after you have found a
   target (to re-detect roaming targets).
   
-   Unitscan will alert you of NPC targets that you can attack and are
   alive.
   
-   **Unitscan will pause scanning when in combat or when auto attack, auto shoot and wanding are active.**  
-   **Please note unitscan-turtle will not auto target the target when it is found.**    
   **Click the target in the unitscan window or use the macro /unitscantarget to target the mob.**

## Commands / Use
**You can move the unitscan frame by holding CTRL+SHIFT+LEFT CLICK dragging.**


**/unitscan** *lists the active scan targets*    
**/unitscan name** *adds/removes **name** to/from the active scan targets*    
**/unitscantarget** *targets the most recently found target*    

You can add custom targets to find players or targets not included in the zone targets list by using the command /unitscan *name*. 

Please Note: Targets added using /unitscan *name* will be removed from active scan targets after they are found. For a permanenet solution, edit [zone targets.lua](https://raw.githubusercontent.com/RetroCro/unitscan-turtle/master/zonetargets.lua) and add a line entry for that unit.

## Complementary Addons
[**SoloRaidTargetIcons**](https://github.com/refaim/SoloRaidTargetIcons) - This addon lets you put raid markers on units without being in a party (see video).

[Codex](https://github.com/nakda/codex/tree/main) - To see target abilities in the tooltip.

## Addon Compatibility
Unitscan uses the [TargetByName](https://wowpedia.fandom.com/wiki/API_TargetByName) function to scan through the list of targets to find an exact match. This causes the game to switch targets if the named target is nearby. Unitscan will immediately restore your original target however if you are using addons that do something when you switch targets (such as issue an alert if targets are PvP flagged) then they may trigger for the found target.
