----------------------------------------------------------------------------------------------------
xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx
----------------------------------------------------------------------------------------------------

xxx---- Crispy HUD Addon for SidHUD ----xxx

contains optional addons for
- SquareDOV 		retexture and text-color-adjustment (blueish clock and static counter)
- AlternativeIcons 	rescaling-patch (to fit with the new HUD/ also compatible with the CY-A HUD by ISayRandomThings)
- CrispyHUD 		enable quickslots and currentammocounter patch


INSTALLATION:

for best results use ModOrganizer2 or your prefered mod installer -> fomod
!!! however make sure you load CrispyHUD addons after SidHUD, SquareDOV or AlternativeIcons since any of my patches/addons needs files from these mods !!!
optional addons can be used seperately aswell, they do not require the use of CrispyHUD files

or

manually install the files via classic copy paste to .../anomalydir/gamedata
!!! with this method you have to be careful tho and install the other mods first and then my addons/patches last !!!

----------------------------------------------------------------------------------------------------
xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx
----------------------------------------------------------------------------------------------------

changes:
fixed up and redone elements of CY-A HUD Addon for SidHUD
-- ammo counter, weapon health, armor health, rad bar, psy bar, hp, bleeding - adjusted textures
-- now you can toggle the items on and off again separately, from MCM menu in SidHUD
-- additional patch included to bring back Quickslots and CurrentAmmoCounter(magazine)(install after CrispyHUD main addon)
-- simple retexture that fits the minimal HUD style

optional
-- retextured SquareDOV	Minimap Mod to fit the new theme
-- font-color-adjustment for SquareDOV Minimap Mod, turns the clock and "NPC-counter" under the minimap blue-ish
-- rescaling-patch for AlternativeIcons Mod, Buff/Debuff icons downsized to .38 (works for CY-A HUD aswell)

highly inspired by CY-A HUD! check it out first before you download my version!
https://www.moddb.com/mods/stalker-anomaly/addons/cy-a-hud

SidHUD needs to be installed first, for this mod to work
-- make sure CrispyHUD is loaded after SidHUD !!
https://www.moddb.com/mods/stalker-anomaly/addons/sidhud

SquareDOV Minimap Mod needs to be installed first, if you want to use the minimap retextures/recolors
-- i recommend using this along with the MinimapToggle Addon to keep the game more immersive
-- make sure CrispyHUD/Addons is/are loaded after SquareDOV !!
https://www.moddb.com/mods/stalker-anomaly/addons/squaredov

AlternativeIcons needs to be installed first, if you want to use the rescaling-patch
-- you can use any of the colors when installing, i recommend the coloredIcons version
!! colors and textures and not included in my patch !!
-- you must install Alternative Icons first -- 
-- make sure this patch is loaded after Alternative Icons !!
https://www.moddb.com/mods/stalker-anomaly/addons/alticons

----------------------------------------------------------------------------------------------------
xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx
----------------------------------------------------------------------------------------------------

all credits go to the respectable authors of these mods:

Strogglet15, RavenAscendant, BlackGrowl, Tronex, ISayRandomThings

----------------------------------------------------------------------------------------------------
xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx
----------------------------------------------------------------------------------------------------

Hello Stalkers, QuickInfo!

quickslots, current magazine count or the current ammo icon
edit the maingame.xml/maingame_16.xml found in gamedata/configs/ui of my modfolder or
if already installed your gamedirectory / modloader mod dir
find these lines (either use Notepad++ and look for the nr of the line or Ctrl+F/scroll around till you find it)
alternative to installing the patch i made you can scroll through the document keep an eye open for quickslot and change the values that are above 1k, 
down from "11xx" to "xx" (careful static_cur_ammo only needs 1 number removed so x="173" for ex.)
like this you can move and edit the Ui elements by yourself if you feel the need to tune something or adjust.

!!! i recommend you keep the ammo icon offscreen !!!
but you can always play around with the x" and y" values and find a spot where you prefer it. 
-for some reason stretch="1" does not work for me on this and i therefore cannot change the size of that icon
-currently it sits ontop of the hud, does not fit in well and clips a little bit of the PDA icon
-change x to "120" from "1120" to enable it
-to adjust the value yourself you can find it by looking for static_wpn_icon in the maingame/maingame_16.xml

----------------------------------------------------------------------------------------------------
xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx
----------------------------------------------------------------------------------------------------
for enabling quickslots 
find and replace these lines at 112-153:

    <quick_slot0 x="22" y="705" width="15" height="17" stretch="0"> 
	<counter x="1" y="60" width="15" height="9" stretch="0">
			<window_name>counter</window_name>
	<text font="small" x="-2" y="-69" align="c" vert_align="c" r="238" g="155" b="23"/>
	    </counter>
    </quick_slot0>
    	<quick_slot0_text x="33" y="827" width="17" height="13">
        <text align="c" vert_align="c" font="letterica18">quick_use_str_1</text>
    	</quick_slot0_text>


    	<quick_slot1 x="40" y="705" width="15" height="17" stretch="0">
	<counter x="1" y="60" width="15" height="9" stretch="0">
			<window_name>counter</window_name>
	<text font="small" x="-2" y="-69"  align="c" vert_align="c" r="238" g="155" b="23"/>
	    </counter>
    </quick_slot1>
    	<quick_slot1_text x="73" y="827" width="17" height="13">
        <text align="c" vert_align="c" font="letterica18">quick_use_str_2</text>
    	</quick_slot1_text>


    	<quick_slot2 x="58" y="705" width="15" height="17" stretch="0">
	<counter x="1" y="60" width="15" height="9" stretch="0">
			<window_name>counter</window_name>
	<text font="small" x="-2" y="-69"  align="c" vert_align="c" r="238" g="155" b="23"/>
	    </counter>
    </quick_slot2>
    	<quick_slot2_text x="113" y="827" width="17" height="13">
        <text align="c" vert_align="c" font="letterica18">quick_use_str_3</text>
    	</quick_slot2_text>


    	<quick_slot3 x="76" y="705" width="15" height="17" stretch="0">
	<counter x="1" y="60" width="15" height="9" stretch="0">
			<window_name>counter</window_name>
	<text font="small" x="-2" y="-69"  align="c" vert_align="c" r="238" g="155" b="23"/>
	    </counter>
    </quick_slot3>
    	<quick_slot3_text x="153" y="827" width="17" height="13">
        <text align="c" vert_align="c" font="letterica18">quick_use_str_4</text>
    </quick_slot3_text>

----------------------------------------------------------------------------------------------------
xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx
----------------------------------------------------------------------------------------------------
for ammo icon(static_wpn_icon),current ammo in magazine(static_cur_ammo) 
find these lines and replace them at lines 206-231:
		
		<!-- put a thousand in part's "x" to get rid of a part -->
		<static_cur_ammo x="173" y="746.0" width="14" height="19">
			<text align="1" vert_align="c" complex_mode="0" font="graffiti22" r="255" g="255" b="255" a="255" >ammo</text>
		</static_cur_ammo>
		
	    <static_fmj_ammo x="1164" y="734" width="26" height="15"> 
	        <text align="1" complex_mode="0" font="small" color="ui_7">fmj</text>
	    </static_fmj_ammo>
		
	    <static_ap_ammo x="1164" y="728" width="26" height="15"> 
	        <text align="1" complex_mode="0" font="small" r="238" g="255" b="235" a="150">ap</text>
	    </static_ap_ammo>
		
		<static_third_ammo x="1164" y="722" width="26" height="15"> 
	        <text align="1" complex_mode="0" font="small" r="238" g="255" b="235" a="150">third</text>
	    </static_third_ammo>
		
	    <static_grenade x="150" y="750.5" width="14" height="19"> 
	        <text align="c" vert_align="c" complex_mode="0" font="small" color="ui_7" >gr</text>
	    </static_grenade>

		<static_wpn_icon x="1120" y="705" width="20" height="26" align="c" alignment="c"/>
	
		<static_fire_mode x="162.5" y="743" width="14" height="19">
	        <text align="c" vert_align="c" complex_mode="0" font="small" r="255" g="255" b="255" a="255"/>
	    </static_fire_mode>
		
----------------------------------------------------------------------------------------------------
xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx
----------------------------------------------------------------------------------------------------

keep pushing through the Zone!

created by SavageBulldog

----------------------------------------------------------------------------------------------------
xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx
----------------------------------------------------------------------------------------------------