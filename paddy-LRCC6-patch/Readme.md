## WARNING

Are you sure you want to try this? Due to the nature of how Paddy works at startup (poking at menus), it can cause a lot of trouble.  And takes effort from you. There is no easy install provided, and extra hoops to hop through for you to intentionally do this.

No assurances that it will work for you. Worked for one other person I know, worked for me. Deveop mode. Library mode bugs were not patched. On Win7/LR CC v6 (2015.10), Win10/LR CC v6 (2015.10), Win10/LR CC v6 (2015.13, this is the last known update as of 2017 October); English. 

Not tested and likely to have issues with LR6 non-CC version. 

Will very likely cause issues with LR Classic CC (version 7). 

## Requirements and Recommendations

* Paddy, the last LR5 beta, installed and working for you in LR 5.x. "Latest" on sourceforge was Paddy.lrdevplugin 5.2Beta2.zip.
* Even in LR 5.x, some sliders will not focus correctly with Paddy-LR5.
* Have LR CC 6, but Paddy disabled (Paddy-LR5 should complain first start and exit itself). Have a test catalog of one image.
* LR set to English. The old code attempted to be multi-language. On examination, even the German preferred translations in Paddy-LR5 were lagging and items still existed that were hardcoded. All other languages were in disarray. Paddy was bound to ANSI and no UTF/Unicode support.
* IMPORTANT: Your LR interface (Library and Develop) should be set to all panels active, and all of them open. aka "Expand all panels". Not solo mode. IMPORTANT: Any and all the sub panel items in Library/Dev mode should be expanded (all the little black triangles in any panels, such as Quck Develop -> Tone Control, should be pointed down) before attempted use.
* You should have a "dummy/test/virtual copy" image that you last open/close your catalog with. Paddy's "pokes" on the UI can inadvertently create some items on your history stack 

#  IF YOU REALLY WANT TO.

A binary diff is provided for patching via jojodiff utility

10 steps to create one .exe? Why was it not uploaded? The steps are intentional to ensure your intent and will to want this. After you create the paddy.exe and want to distribute it on another github/sourceforge, that's your call. I did not want to deal with support issues with people just trying it for fun.

If you think the steps are wrong, do a screen recording showing Paddy-LR5 working in LR5 for you, then starting LR6 with Paddy complaining, then Paddy being disabled in plugin manager; follwed with a recording from the start of the steps below to show that you followed did every step and it failed to run, I'll consider it an issue to be perhaps dealt with; just create an Issue and link to the video.

1) Ensure Requirements and Recommendations above have been followed.

2) You must have the right Paddy 5. To check, in your %appdata%\Adobe\Lightroom\Modules\Paddy.lrdevplugin\Paddy\, there is a Paddy.exe. It MUST have a sha-1sum of 81828baf0abaaa99a2d2ee24b38435b56c29cb4a or sha-256 of 90007515a4815c91207d769d1f4d8623c279ddbc2b0735f4ba9f6b2c99eae0e9. If you are unsure how to check a hash, upload your paddy.exe to http://www.virustotal.com. On the detail page, you should see "SHA-256	90007515a4815c91207d769d1f4d8623c279ddbc2b0735f4ba9f6b2c99eae0e9" IF THE SHA-256 SUM IS DIFFERENT. YOU HAVE AN INCOMPATIBLE LR5 Paddy. Recheck.

For example. https://www.virustotal.com/#/file/90007515a4815c91207d769d1f4d8623c279ddbc2b0735f4ba9f6b2c99eae0e9/details

3) You will need jojodiff, a binary diff/patch utility. https://sourceforge.net/projects/jojodiff/ Download, extract the files somewhere. Let's call it c:\jojodiff. There should be a file called jptch.exe

4)  BACKUP your %appdata%\Adobe\Lightroom\Modules\Paddy.lrdevplugin\ This patched version WILL NOT work for 5.x. You will need your backup.

5) Download paddy5-to-6-patch.jojodiff from here. To c:\jojodiff as well

6) Make a copy of your paddy.exe to c:\jojodiff as well, and rename it Paddy5.exe

7) Open a Command Prompt (e.g. win+r key, enter cmd.exe), enter these two lines, changing the directories if you used something other than c:\jojodiff
cd /d c:\jojodiff
jptch.exe Paddy5.exe paddy5-to-6-patch.jojodiff paddy.exe

8) Check that your new paddy.exe is correct (hash yourself or with virustotal.com). This paddy.exe for LR6 CC 2015 should be:sha1sum 3c29dff5905ae8f2e20331abd960d3034915d3a1 or SHA-256	60fc316ad7a9d0c67fff5e1276f7c26d54d7043ac0293859f1ef5599d0bdbc22

For example. https://www.virustotal.com/#/file/60fc316ad7a9d0c67fff5e1276f7c26d54d7043ac0293859f1ef5599d0bdbc22/details

9) Copy this new paddy.exe from c:\jojodiff and overwrite (WARNING: you should have backed up in step 4) the one in %appdata%\Adobe\Lightroom\Modules\Paddy.lrdevplugin\Paddy\

10) Fire up LR6 CC 2015. Enable Paddy from plugin manager. Paddy should no longer complain about not being in LR5. Be patient and let it do it's UI scanning. If Paddy starts in suspended mode (paddy icon with a strikethrough in the task icon area), right click on the icon and restart it. When done, you should be set to use it just like you did with LR5. In the assignment preferences, you should have one new option that allows you to assign a hotkey to selecting the Dehaze slider.

