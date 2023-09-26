
# References
### MCreator Wiki
You can find more information about this system in MCreator on this Minecraft wiki page.  
[https://mcreator.net/wiki/integrating-forge-update-checker](https://mcreator.net/wiki/integrating-forge-update-checker)

### Example File
You can find an example file here:  
[https://github.com/MCreator-Examples/Projects/blob/main/examples/mod_update_file/updates.json](https://github.com/MCreator-Examples/Projects/blob/main/examples/mod_update_file/updates.json)

# Code Breakdown
### Home Page
This home page can be used to let people know in-game when there is a new version of your modification.  
  
It will direct traffic to the page you provide.  
  
At the end of the last quote " " you should put a comma but only if it's not the last line.
```json
{
  "homepage": "https://www.curseforge.com/minecraft/mc-mods/cctv-craft",
}
```
### Changes Section
The first set of numbers (1.20.1) controls the Minecraft version the update is for, this is later used in the Promos section below this section.  
  
The second series of numbers inside the brackets "{ }" of the Minecraft version is used for your mod build version.  
  
At the end of the last quote" " you should put a comma but only if it's not the last line.  
  
You also need a comma at the end of the closing bracket for each Minecraft version that the mod supports "},"  
  
You can make new lines using the backslash followed by a lowercase "n" like this "\n".

```json
{
  "1.20.1": {
    "1.4.1": "Fixed an issue with spawn rates for the entities.",
    "1.4.0": "Ported the modification\nAdded river plans\nAdded New 3 new entities Ox, Deers, and Boars"
  },
  "1.19.4": {
    "1.3.0": "Added grappling hook\nAdded flax crops\nAdded blue mushrooms to caves",
    "1.2.0": "Added 5 new biomes\nAdded pine, maple, yew, cedar trees",
    "1.1.0": "Ported the modification\nAdded custom dimension called Blue Skys\nAdded flares sticks"
  },
  "1.19.2": {
    "1.0.0": "Added limeston\nAdded Rocky Dirt\nAdded Healing Water"
  },
}
```
### Promos
Promos control what version your latest and recommended builds are.  
   
In most cases the version will be the same unless you are not sure if the latest version is stable, in this case, keep the recommended version on the last known stable version.  
  
The Minecraft version should be before the "-latest" or "-recommended" The value of these lines relates to the builds listed above in n the changes section the mod version should be the value of the promos lines.  
  
Also inside the promos section, each line should have a comma except the last line.  
  
And lastly the closing bracket at the end of "promos" "}" should not have a comma as it's the last bracket in the list of the main object.
```json
{
  "promos": {
    "1.20.1-latest": "1.4.1",
    "1.20.1-recommended": "1.6.1",
    "1.19.4-latest": "1.3.0",
    "1.19.4-recommended": "1.3.0",
    "1.19.2-latest": "1.0.0",
    "1.19.2-recommended": "1.0.0"
  }
}
```

### Using GitHub for hosting.
In order to host the file you need a public GitHub repository for hosting the JSON file.  
  
You can either upload a file you have or create a new file with .json at the end.  
  
Once you have the file you can use the template below and make changes to what you need for your versions.  
  
After you have changed the file you can view the file and click the "Raw" button this will open a new page on GitHub.  
  
Once you are on this page copy the page URL and paste it into your MCreator update JSON section in your mod settings.  
  
Your URL should look like something below.  
"https://raw.githubusercontent.com/northwesttrees-gaming/CCTV-Craft/main/updates.json"  

# Full Example
A full example can be found below of the code parts used in this tutorial.
```json
{
  "homepage": "https://www.curseforge.com/minecraft/mc-mods/cctv-craft",
  "1.20.1": {
    "1.4.1": "Fixed an issue with spawn rates for the entities.",
    "1.4.0": "Ported the modification\nAdded river plans\nAdded New 3 new entities Ox, Deers, and Boars"
  },
  "1.19.4": {
    "1.3.0": "Added grappling hook\nAdded flax crops\nAdded blue mushrooms to caves",
    "1.2.0": "Added 5 new biomes\nAdded pine, maple, yew, cedar trees",
    "1.1.0": "Ported the modification\nAdded custom dimension called Blue Skys\nAdded flares sticks"
  },
  "1.19.2": {
    "1.0.0": "Added limeston\nAdded Rocky Dirt\nAdded Healing Water"
  },
  "promos": {
    "1.20.1-latest": "1.4.1",
    "1.20.1-recommended": "1.6.1",
    "1.19.4-latest": "1.3.0",
    "1.19.4-recommended": "1.3.0",
    "1.19.2-latest": "1.0.0",
    "1.19.2-recommended": "1.0.0"
  }
}
```
