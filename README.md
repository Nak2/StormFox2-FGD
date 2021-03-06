# StormFox2 FGD

   The resources for Hammer to intergrate StormFox 2 entities, functions and settings (For V2.50 and above).  
   The goal is to implement these entities into other similar mods.  

   There are also two prefab logic_relays prefabs for day / night, that should work with any day / night mod.  

## How to install
- Download the zipfile https://github.com/Nak2/StormFox2-FGD/archive/refs/heads/main.zip
- Unzip the content to your Garrysmod folder: SteamLibrary\SteamApps\common\GarrysMod\
- Open Hammer
- Click on "Tools" -> "Options"
- At "Game Data files:" click on "Add"
- Select the file "stormfox2.fgd" and click "Open".
- Click "OK".
 
The content includes model, textures and the FGD to use.

## "I only want to use the FGD"
  You can download the FGD here: https://github.com/Nak2/StormFox2-FGD/blob/main/bin/stormfox2.fgd  

   The FGD has to be placed within the "bin" folder of Garrysmod.  
   Follow the same steps as above.

------------------------------------------------------------------

#### Relay Entities
<p><b>Note</b>: For best results, it is best to stick to one relay of each type. Making multiple relays of the same type, can confuse Source when it comes to light.</p>

- #### logic_day_relay

   A relay entity that can be configured to trigger doing day or when the light should turn off.  
   <b>Note</b>: Some weather types modifies the lightlevel of the map, causing light to turn on / off.   

- #### logic_night_relay
   A relay entity that can be configured to trigger doing night, or when light should turn on.  
   <b>Note</b>: Some weather types modifies the lightlevel of the map, causing light to turn on / off.  

- #### logic_weather_relay
   A relay entity that trigger when specific weather-conditions are meet.  
   List of default weather-types: 'Clear', 'Rain', 'Snow', 'Cloud', 'Fog' and 'Lava'.  
   <b>Note</b>: Might still be a bit buggy  

- #### logic_weather_off_relay
   A relay entity that trigger when a specific weather-condition are turned off.  
   List of default weather-types: 'Clear', 'Rain', 'Snow', 'Cloud', 'Fog' and 'Lava'.  

- #### logic_temperature_relay
   A relay that gets triggered when temperature is within a range.  
   Note</b>: This relay runs on a 3 second interval.  

- #### logic_time_relay
   A relay that gets triggered when time is within a range.  
   <b>Note</b>: This relay runs on a 3 second interval.  

- #### logic_thunder_relay
   A relay that gets triggered when it starts or stops thundering.  

#### Set Weather
- #### logic_weather_relay
   This entity holds weather-data that can be set when triggering "SetWeather".
   It also allows you to set varius of weather-settings like wind and temperature.
   Note</b>: It has a 2 second cooldown, before it accept "SetWeather" again.

#### Setting Entities
These entities hold settings that StormFox 2 will utilize (Unless the user overrides them).
- #### env_stormfox2_settings
   Holds a list of default settings.  

- #### env_stormfox2_materials
   This entity will disable the default material-scanner and allow you to handpick 12 materials and set the material-type. 
   You can always spawn multiple entities, in case you need to use both material-types or more materials.  
