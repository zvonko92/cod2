Browse to your Call of Duty 2 installation folder. Right-click on "CoD2MP_s.exe" and click "Copy". Go to your "Desktop" and "Paste Shortcut"

Right-click on gameserver shortcut and go to "Properties"

In newly opened window go to "Shortcut" tab if you're not there already. The field we are interested in is "Target". 
After CoD2MP_s.exe path add space and append following lines:

+set dedicated 1 +set sv_pure 1 +set fs_game "mods/zpam207" +set sv_punkbuster 0 +set g_gametype sd +set sv_hostname "LAN GS1" +set net_port 28961
mods/zpam207/zpam207.iwd

Head back to to your installation folder and there create folder mods/zpam207. Place zPAM207.iwd in that folder:
NOTE: We could've also skipped this step, removed fs_game variable from above steps and just added all mod files to main folder, 
but we wanna play it nice, these settings were made for a reason and the best practice is to honour them.

At this point servers are up and running but the games are not initialized. For this to happen we need to set the map for the first time. 
Enter in console "map mp_toujane"
set rcon_password ""
pam_mode cg

Your servers are now ready for play. People connected to your Local Area Network should be able to see it from ingame browser, 
but in case they don't or you want to immediately find out your server IP you can do it by launching "cmd.exe" from Start Menu and running "ipconfig" command:
We are interested in IPv4 Address. In this case if a player wants to connect to GS3, the command would be
/connect 192.168.1.10:28961



//"source: https://eu.letsplay.live/forums/thread/607458/How-to-setup-LAN-servers/"//

