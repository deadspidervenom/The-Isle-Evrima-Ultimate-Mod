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
