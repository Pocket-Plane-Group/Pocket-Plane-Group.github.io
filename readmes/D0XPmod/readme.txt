                                   Ding0 Experience Fixer
                           A Product of the Ding0's Nefarious Mind
                               http://www.pocketplane.net/sim/

                                   Version 7 (updated by Angel)

- The mod that always needed making!
- A unique exercise in WeiDU coding!
- A lovingly crafted readme!
- Who says minimalism isn't good for making the game harder?


Section I: Introduction
-----------------------
BG2 allows you to attain ridiculously high levels. While I frequently see suggestions for
removal of the XP cap to allow people to reach levels higher than 50, rarely do I see
anyone mention the idea of LOWER levels. That's what this mod's all about.
Some of the BG2 XP rewards are, frankly, ridiculous. Tens of thousands of XP each for
simple Fed-Ex quests? Not so, I say.
Ding0 Experience Fixer (or DEF JAM, as it's otherwise known; feel free to imagine what the
JAM part stands for) allows the XP rewards to be reduced. Split into 3 separate sections
(creature XP, skill XP and quest XP), you can choose the new XP rate for each component
irrespective of the others. Choices vary from 10% to 75% of the original XP.
Who knows. Maybe 10% XP rewards would provide a challenging alternative to Tactics-type
mods.

Intallation note: The Quest XP component is very sensitive to broken dialog-
or script files left by other mods, or in the game itself if you do not have
the G3 Fixpack installed (which you should have installed, really).  If you
get warnings upon installing this mod, this is the most likely cause.  The
Fixpack should be installed before this mod (and, in fact, most other mods).

Also note that for the starting XP patches to work correctly with ToB, you must have the
BGMAIN.EXE file from the v26498 ToB patch.


Section II: Installation
------------------------
BGII and ToB are required. The mod should work fine with most other mods (including
all of those created by the Pocket Plane team).

Unzip the main ZIP file into your BGII main directory. This is normally:
        C:\Program Files\Black Isle\BGII - SoA\

Run (click on) "setup-xpmod.exe".

Then choose which components you would like to install. They are all optional. You may
always uninstall any or all of them later by re-running "setup-xpmod.exe".

The mod may work correctly without starting a new game, but it is strongly recommended
that you do so.

The components should install correctly for international players who have both
DIALOG.TLK and DIALOGF.TLK. No game text is added, so translations are irrelevant.


Section III: Known Issues & Compatibility
-----------------------------------------

This mod can be installed on vanilla BG2 (with or without ToB), Tutu (with or
without TotSC) and BGT.  Compatibility with vanilla BG1, the Icewind Dale Saga,
Planescape and the Enhanced Editions of BG1 and BG2 is currently untested.
The starting XP component will definitely not work on these, but the others might.

BG2 should be updated to official patch v26498 (the GoG version already
includes this patch).  You should also have the G3 Fixpack installed; this mod
can work without it but you will see tons of warnings and may have other
issues.  Install Fixpack before this mod (and indeed before most other mods).

This mod should be installed as late as possible, at least after all other
mods that introduce new creatures, quests or other sources of experience, or
meddle with the XP tables in any way.  Any sources of XP introduced by mods
installed after this one will not be affected.

There is one known issue if you have the BG1NPC mod installed (on Tutu or BGT)
and try to install the Quest XP component.  This may (especially on Linux) fail
with an error saying that "NEWMERCH2.DLG" cannot be found.  This is a faulty
file left by BG1NPC.  Deleting this file from the override folder should fix
the issue and allow normal installation.
(This file is not used by anything, and cannot actually be used properly.
Note that the filename without extention has 9 characters, files for the
Infinity Engine should are restricted to 8 because that's the maximum number
of characters in all resource fields in the various structures.)

Other than the issue above, no incompatibilities with other mods are known at
this time.


Section IV: Thanks
-------------------
Weimer, for implementing the most obscure WeiDU commands imaginable to make this possible.

Japheth and CamDawg, for helping me sort out the coding.

This mod was created entirely With WeiDU. :)


Section V: Version History
---------------------------
1 - Initial release.
2 - Should work with BG1 and SoA-only installs too.
  - Added option for 0 XP rewards for learning spells.
  - Added option to modify starting XP.
3 - TRAified.
4 - Added solo-specific stuff.
  - Cleaner coding.
5 - Added French translation by Graoumf and Spanish translation by Ghildrean.
6 - Improved compatibility with BGT.
  - Suppress trivial install-time dialogue warnings.
  - Added German translation by Garret.
7 - This update was done by Angel.
  - Updated to WeiDU 237.
  - Thorough code overhaul, close to an almost complete rewrite actually.
    A few highlights of code improvements:
    - The size of tables (2DA files) is now dynamically determined instead
      of assumed, this should improve inter-mod compatibility, especially
      with experience cap removers and other mods that implement level 50
      rules.
    - READ_2DA_ENTRIES_FORMER and SET_2DA_ENTRY_LATER are used for speed
      when patching tables.
    - All instances of DECOMPILE_BCS_TO_BAF and DECOMPILE_DLG_TO_D have
      been replaced with DECOMPILE_AND_PATCH.
    - The Quest XP component will now dynamically search for and patch
      XP-granting spells instead of simply patching a few hard-coded ones, so
      if any other mods add such spells this mod will patch them too.
  - Options have been added to actually increase experience given by
    creatures, tasks or quests to 150% or 200% (requested by Salk).
  - 0 XP rewards for spells will now actually affect learning spells only as
    advertized and leave the XP awards for locks and traps alone.
  - Cleaned up the folder structure a bit and moved all translation files
    to the "lang" folder.
  - Made the mod more Linux-friendly by lower-casing all files.
  - Worked the bug fixes from the BWP Fixpack into the new code.


