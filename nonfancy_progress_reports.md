This file is a non-fancy progress report one what is being worked on, what is done, what is confirmed and ect.

The intent is just to have something to post until the mod is at a stage i feel is ready to release.

These posts will be vague to keep various methods a secret until they are protected on the AGPL-3.0 license

---------------------------------
7/8/2026 ~ Big first report
---------------------------------

Got ahold of a friend and did some testing, i confirmed that the auto-linking is almost complete. I made the oversight of forgetting that computers and routers need portforwarding, so while i did confirm that it SHOULD be functioning(by mistake of all things). I need to add port forwarding to the mumble plugin to make it actually work.

Due to time constraints of my friend and the time needed to add in automatic portforwarding, i was unable to confirm the functional state of the VOIP. We made plans to meet up later to test it after i get the portforwarding implemented.

Going forward after the portforwarding issue is fixed, ill be working on trying to eliminate hardcoded values that either make updating an issue, or make configuring time consuming.

For the server that is an easy task, however for the mumble plugin it is tricky due to the non-native nature of this plugin support. I have a solution i thought up, and while it is a bit janky, if it works it will mean that 1 plugin will work for any server using the code from my mod.

After all that is said and done, ill be re-coding the dino restore function. First testing methods that would be ideal if they work. if they fail then manually building a custom method. Ill also be working on fixing the chat logger. While i had it working in previous interations of this project, in this one it has been broken and simply put on the back burner due to the lack of importance.

Once i get all of the "working on" code fixed and ready, i will be adding in the dino save and load feature since most of the ground work will be done thanks to the admin dino restore. That will also come with a companion app, the graphics for it won't be anything special, but it will work.

After that i will release the 1.0 of the code here, along with instructional materials.

---------------------------------
7/10/2026 ~ R&D plus some groundwork
---------------------------------

i did some testing and research as i was still waking up when i wrote the last update. When i woke up more i realized "it cant be a portforwarding issue im the host not my friend" so to not just go with what i assumed first i did some research and confirm it was likely a windows firewall issue.

As such going forward i will be bundling a install and unistall bat file with the source and release version of the mumble plugin. This install(and uninstall but in reverse) bat simply moves the plugin into the plugin folder and allows mumble (the plugin goes through mumble in this situation) through the firewall on the needed port. Of course the uninstall reverts this.

The reason i chose a bat instead of an EXE was for piece of mind of people using this project. They can see EXACTLY what the install is doing and why. They do not need coding knowledge to see understand.

Outside of fixing that issue (hopefully) i did some other work.

I've sectioned off some of the features to be able to toggle them (was not orginally in the code due to scope changes). I also made all options config and offsets not hard coded for the server mod.

From there i did a bit of groundwork to finish up the rest of the features. The current list of "working on" features are pretty close to done. the voip only needs testing to confirm it is done, the auto-linking is half almost done, with the other half being worked on now. The first half that is almost done needs testing still but once confirm done the focus will be on finishing up the auto-link. 

After i finish the autolinking i want to get the chat logger working. The main reason is just to have all features that are "in progress" with actual functioning code completed. Then i can R&D the admin dino restore feature know full well the rest of the features are functioning, so if i break anything during R&D i can fix it.

During that time i will also be making a basic companion app to use with the admin features. Which is another reason i am saving it for last. As there is a lot i want to include in the companion app functionally wise. Visually it will be very basic though.

Once all features are built and tested, i will clean up the code for any loose dead ends, make instructional documents, do some minor improvements via including a few public libraries that are okay to use with this projects license. Then release V1 of the plugin source.

After that i will begin work on the other potential features. I hope everyone watching this project stays patient with me. This project while slow to develop is because i like quality and i want to make sure when i release this it functions as close to what i want as it can get.

---------------------------------
7/12/2026 ~ Plan changes
---------------------------------

So as i was working to finish building the rest of the main features. I realized i needed to get the chat logger working before i could do part of it. So i got that working, then during that i realized some of the features i had been working on would be better suited to be done via the companion app. So i have started work on the start of that.

Meaning right now the current progress of the "working on" was put on hold till the companion app is functional. I did however figureout a way to improve the VOIP audio. I am still missing 1 piece of information from making it perfect, however i tried my best to find that and i believe it is not update server side.

For the companion app i am also intergrating a admin panel system into it. As well as a primitive anti-cheat. Don't worry it wont effect performance the anti-cheats purpose is to simply log when something weird happens and reject data or attempts from it. The admin will have to manually review cheating attempt and punish if they believe it was the case.

Due to companion apps need to be developed some systems will be developed early, though bare bones. Namely the point system and affiliate system. Why those 2? For points it was an easy to add in, and made it so we did not need place holder GUI elements involving it. Plus it makes intgration easier for future features. For the affiliate system, it originally was not gonna be added since i did not know if the gui i was thinking of using for this project was gonna work with a web based things. However turns out it handles it fine, so it will be added in.

Currently how points will work is there will only be 2 ways to earn points on initial release of this mod, play time and watch time. I plan to configure it so you can adjust how much each content creator earns you for watch time independantly. The main reason behind that choice is because i wanted to add in more platform compatibility.

Outside of that the main things that will be functional will mostly be admin stuff. I'll be adding a full admin suite, you will have access to rcon, logs, config options, edits of player data and ect. All of it will be remote as well, so you wont need to be at the PC the server is hosted on.

Now you may ask what about security? Everything is handled on the server end of things. I wont go into details till the mod is released, but the server will know who is connecting, and if the data you can't spoof or use to be someone else does not match any existing user or admin(depending on what you are trying to do), any data you try to use or do gets dropped and you info is logged.

Just keep in mind just because a user gets logged as suspicious does not mean they are 100% cheating, there can be cases where something looks like cheating via a log but turns out not to be. So any logs you find investiage. There will be an error code that gets posted if someone does try to cheat. If they dont know better they will post it.

Outside of that most of the companion app will be just a shell of "TBA" and such. That does mean every feature i plan to add will have a tab for when it does get added, but for now its static.

On a side note the recent game updates have been infuriating due to manually needing to update the offsets 3 times now. Thought the most recent update was odd since none of the offsets i use got changed. Not even the main ones even though the base offset was different.

I will also be adding in external libraries to hopefully future proof and optimimize the code for very large servers. More so since this mod will be very heavy on what it does server side.

Lastly before i go i have started work on updating my reference docs as well as putting together instructional docs. So as soon as all the working on features are complete i can post everything and begin working on other features.

---------------------------------
7/15/2026 ~ Not much to report
---------------------------------

I am making this just to update with something. The Companion app is taking longer then i thought, mostly due to time constraints and how much is needed to make sure this is a quality i can accept.

Currently i got a barebones app made, it can connect to the server, get credentials and reuse them, track suspicious activity(people attempting to cheat or spoof info), and thats about it.

Most of the work was on the game server side of things. Making the credentials system, the suspicious activity logs, clearing logs that were false flags, and connecting the companion server into the rest of the mod to streamline some stuff.

Now that most of the corner stone stuff is done, all thats really left of the planned stuff for the app before going back to adding in the "working on" features, Is mostly TBA panels, admin panels to make my life easier, the skeleton of the points system, and the affiliate system.

After that ill begin work on the "working on" items, i first need to rework the plan a bit (to account for the companion app) but aftwards the rest should go up fairly fast.

One thing i may work on adding is stuff for sending in game chat messages. Thanks to diplomatic-tendencies over on their [github](https://github.com/diplomatic-tendencies/evrima-dev-knowledge) i was able to learn why my methods of sending messages kept crashing the server. Please feel free to check their github out if you want to try making your own ue4ss based mod.

---------------------------------
