Alright so, how this works is it's sorta like a plug & play system

All you've gotta do is go find the bundle containing the model of the character you wish to replace, which the first part of this guide here will tell you how to do (That's really all you need from the guide as I've done the rest for you): https://docs.google.com/document/d/1oHPVuzExqDpGqEYbpEadEI6mccATe8BN_wtuRtNHR6s/edit?usp=sharing, open it up in Asset Bundle Extractor (https://github.com/SeriousCache/UABE/releases/tag/v3.0-beta1), then replace the character's mesh object with the .json file of the unit you want from the convienently labeled "Dumps to Import" folder by selecting it, hitting import dump, and switching file type to .json
Note: I'm unsure if you can put the standard models on the winged characters, or if you can put winged characters over standard ones

Next you've just gotta select the Texture2D object, hit Plugins > Edit > Load, and then select the texture you wish to use, hit OK, then accept the slow quality setting, and wait a bit until the modified star appears next to the entry. 

Note: The enemies don't appear to have reflection maps, so they're going to currently use the underlying character's maps which can result in weird shiny bits on the model, I'm currently working on custom ones
Note v2.0: Chief Templar capes are a little funky, I'll try fixing them in v3.0

Then, you just save the bundle, and put it into your game's assets, and voila, you're well on your way to amassing your own army!

If you're emulating and following along with the guide, you should be able to just drag and drop and put them straight into the assets folder, but if you wish to push them to a live device, you can follow these instructions:
Connect your device to your PC and using ADB:
adb push <assetfile> /sdcard/
adb shell
run-as dev.dragaliafound.prod.game cp /sdcard/<assetname> /data/data/dev.dragaliafound.prod.game/files/assets/<ID>/
Where <assetname> is the name of the asset you modified, and <ID> is the first two characters of that asset 

If you have any problems, please contact me on Discord! - Nryder1102#3491