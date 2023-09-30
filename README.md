# rd_rotate

Simplified lua rotation script for AMS2

Based on sms_rotate.lua, but modified to play nice with the emperor server manager by honouring most of the event settings in server.cfg

# installation

1. copy `lua/rd_rotate` to the `lua` directory on the dedicated server install
2. ensure `Enable Lua API` is enabled in the server settings
3. add `rd_rotate` to the `Lua API Addons` in the server settings

e.g.

![emperor settings](img/settings.png "Empreror Settings")

4. start the dedicated server and edit `lua_config/rd_rotate_config.json` as required


# raison d'être

The purpose of this script is to allow more than one race per event with different practice and qualifyication session as the event progresses.

Whilst the sms_script can be used for this, it is rather heavy handed and expects to override many more settings than are sometimes wanted.  This script has a much lighter touch and only overrides the exact settings required.

The example script in `lua_config/rd_rotate_config.json` shows how to run an event with two races, but with the first race having an extend practice time of 300 minutes for only the first race and with a shorter 5 minute qualification/rest period for the second race to allow the grid to be shuffled slightly depending on who wants to try and move back down the grid by not doing a single lap.
