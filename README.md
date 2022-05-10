# Using OBS Studio as an Alternative to NVIDIA Shadowplay


## Table of Contents
This has been formatted in my thinking of a tree, as in the pathing taken to get to it.
- [Introduction](#introduction) 
- [Disclaimer](#disclaimer) 
- [Prerequisites](#prerequisites) 
- [Starting Screen of OBS](#mainWindow) COMPLETED
	- [Profile & Scene Collection](#profileSceneCollection) COMPLETED
	- [Scene Creation & Automatic Scene  Switcher](#scass)  COMPLETED
		- [Scene Creation](#sc) COMPLETED
		- [Automatic Scene Switcher](#ass) COMPLETED
	- [OBSPlay](#OBSPlay) COMPLETED
		- [Known Bugs](#knownBugs)  COMPLETED
		- [How to Setup OBSPlay](#setupOBS)  COMPLETED
	- [Advanced Audio Properties](#aap) COMPLETED
- [Settings](#settings)
	- [General](#general)
	- [Output](#output)
		- [Recording](#output-Recording)
		- [Audio](#output-Audio)
		- [Replay Buffer](#output-ReplayBuffer)
	- [Audio](#audio)
		- [General](#audio-General)
		- [Global Audio Devices](#audio-GlobalAudioDevices)
	- [Video](#video)
	- [Hotkeys](#hotkeys)
	- [Advanced](#advanced)
		- [General](#advanced-General)
		- [Video](#advanced-Video)
		- [Recording](#advanced-Recording)
- [Debugging](#debugging)
- [Making OBS Open on Startup](#obsAutoStart)
- [The Guide Itself](#guide)
- [Credits & Cited Sources](#citations) 

# Introduction (Optional)<a name="introduction"><a/>
Hello, my name is MFGAVIN and what sparked this journey was the hatred for NVIDIA Shadowplay, its unreliable video quality, dogshit audio quality annoyed me, so I journey across the lands of OBS Forums to find the knowledge and ingredients to make an alternative.  And I'm happy to say that I think I pieced enough pieces together to it better than Shadowplay and thought others might enjoy it as well.

 


# Disclaimer <a name="disclaimer"><a/>
First, I'd like to state that this guide is WIP unless I state otherwise.  I'd like to hear all criticism as this is my first time making something like this.  Also, please you the Issues tab for anything you need me for and I'll just 

I'd like to state that most of the information used here was gathered from others and without their pioneering I probably would've had to learn how to code scripts for OBS so thanks to them.

**Also I'd like to state these sections:**
- [Output->](#output)
	- [Recording](#output-Recording)
	- [Audio](#output-Audio)
	- [Replay Buffer](#output-ReplayBuffer)
	
**uses information entirely found in** [StuckInLimbo's OBS-ReplayBuffer-Setup](https://github.com/StuckInLimbo/OBS-ReplayBuffer-Setup) so I do not take any credit for the information presented in those sections.

If others want to use this guide in something, ex: Youtube, then I ask to provide credits to Me as well as all the sources I used.


# Prerequisites<a name="prerequisites"><a/>
I don't want to hand hold so take care of this stuff before starting. 

 - An install of **OBS Studio** (se.live is cringe)
 - Download this [script](https://obsproject.com/forum/resources/obsplay-nvidia-shadowplay-alternative.1326/) from OBS Forums called **OBSPlay**.

# Starting Screen of OBS <a name = "mainWindow"><a/>
## Profile & Scene Collection <a name="profileSceneCollection"><a/>
 
This part only really matters if you have a bunch of scenes and stuff already setup and don't want to screw it up.

So in the main window of OBS if you look at the top you will see **Profile** and **Scene Collection** the purpose of these are to make it able to have completely different settings and scenes apart from your usually stuff.
[Insert Image of Profile and Dropdown Menu]

So with this you can start fresh and be able to follow the tutorial, but again it's not really necessary. 

I'll give you guys my profile and scene collection which can skip most likely the entirety of this guide but you will still potentially have to change them.

Profile:
[Insert ClipRecorder Profile]
Scene Collection:
[Insert ClipRecorder Scene Collection]

## Scene Creation and Automatic Scene Switcher <a name="scass"><a/>
This portion is one of the vital parts of this guide.

### Scene Creation <a name="sc"><a/>
You must follow this as it's important with OBSPlay because of how the prefixes will work with files and folders.

1. Make One Scene Called "Desktop" and add a Display Capture source
2. Add the games you play using Game Captures as it's better for performance

**For LoL:**
	If you're trying to add **League of Legends** and it's not working it could be because of your overlays as it's really stingy, so make sure you check it out, for me it didn't work because of **RTSS Overlay**.  If that do
	
### Automatic Scene Switcher <a name="ass"><a/>
This part's important as it'll optimize the resources when switching to the appropriate from desktop capture and game capture.  

Before I go into more detail, something to note here with this, the replay buffer, and OBSPlay is that whenever you clip something whatever the most recent scene was switched to will result in the file be prefixed to that scene so just remember that when searching for it as it may sometimes be placed somewhere you don't want.

**Go to Tools>Automatic Scene Switcher**
[Image Needed of Automatic Scene Switcher with boxes highlighted]

So looking at the Long Box this is where you need to load up the game and select it then the Short Box needs to be the Scene Name, 

Then look at the **"When no window matches:"** and **select "Switch to:"** and lastly **select "Desktop"**

Leave everything else else as is.
And all that's left is to do that for all the other games you play.


## OBSPlay <a name="OBSPlay"><a/>
What the script does is it makes it able to make folders and or files based on the scene names.  Sadly, the person who made the script was last active July 16, 2021.  And so they're two bugs that I found that I want you guys to be aware of.

### Known Bugs <a name="knownBugs"><a/>
 1. The first bug happens if you want to use **MKV** and want to **automatically remux it to MP4**, it'll cause the **MP4 file to mysteriously disappear into the backrooms** for the entities to enjoy.
 2. The second bug is occurs when selecting the settings for the script so I'll go over it more during the setup.
 
### How to Setup OBSPlay <a name="setupOBS"><a/>
 1. Open **OBS**
 2. Click on **Tools**
 3. Click on **Scripts**
 4. Click on the **+ Button**
 5. Add the **OBSPlay script** from where ever you're keeping it
 6. So for the **Base Save Path** you're going to make a folder inside of whatever the hard drive you chose in **C:/** then make a folder inside of it I made my clips so it would be **C:/Clips/**
 

Now if you follow the steps correctly you should be on this portion 
[Image Needed Here]

**They're 2 Different Modes**
1. Clips will be prefixed with scene name and then go into a singular folder
	1. If this sounds good to you then **check only "Scene Based File Prefix".**
2. Same as Option 1,  but folders will be made according to scene names and the clips will be placed in their according scene folder.
	2. If this sounds good to you then **check both boxes**

## Advanced Audio Properties <a name = "aap"><a/>
Lastly, go back into the **Main Window of OBS** and look at the **Audio Mixer**, and select **Advanced Audio Settings**. After that look at the **tracks** at set it to this.

[Insert Image of Advanced Audio Settings]

# Settings<a name = "settings"><a/>
![[Pasted image 20220509194316.png]]

## General <a name = "general"><a/>
The only section that you may want to know about is called, **"System Tray"**

## Output <a name = "output"><a/>
### Recording <a name = "output-Recording"><a/>
[Insert Image Here of Recording Tab from Output]
 
Leave **Type** to **Standard**

**Set the recording path to the hard drive where you want your clips to be stored**, for me its F:/ but for others it may be C:/ , D:/.  The reason why is because of a bug with OBSPlay and the way it moves files around
[Insert Image of Hard Drives]

 Leave "**Generate File Name without Space**" uncheck
 
 **Recording Format to either MP4 or MKV**.  But remember you cannot utilize the MKV remux to MP4 automatically feature with this script because at the time of writing it makes the MP4 file not show up.
 
**For Audio Tracks**, you can either have both 1 and 2 turned on or just 1 it just depends on your use case since having 2 tracks, one for mic and one for desktop audio allows you to personally customize them later on in editing but its up to you.
 
 **Encoder Options** are going to be slightly varied and so I won't discuss too much about it.  If you have a RTX card go with **NVIDIA NVENC H.264 (new)** since it'd be the preferred use case for me but for you it may be different, so search up if it could be.
 
**Rescale Output**, leave unchecked, but for some people you may have to use it, search up if you may have to because of somethings like monitor resolutions

**Custom Muxer Settings**, leave blank, unless you want to use some of them
  
**Rate Control**, what I've seen others recommend is **CQP**.  
 
**CQ Level**, you should use a range between **14-21**.  A lower CQ Level results in better image quality but a higher file size.
 
**Keyframe Interval** I've seen a couple numbers thrown around so either set it to **0, 2, or 5**.  Though as you can see I set it to 2.
 
 **Preset** can either be either **Max-Quality** or **Quality** you can try the others but I've heard that **Low-Latency options** doesn't do much but once again test it out and see if it's something you want to go.
 
**Profile** it's recommended to use **High** and if you notice problems then to switch to **Main**
 
Leave **Look-Ahead unchecked**
 
Set **GPU to 0**
 
Then lastly for this section, **Max B-Frames to 2**

### Audio <a name="output-Audio"><a/>
Set All the **Audio Track's bitrate to 160** and you can name them if you want to.

### Replay Buffer <a name = "output-ReplayBuffer"><a/>

**Maximum Replay Time** should be set from a range of **30s to 240s** 

**Maximum Memory** should range from **1GB (1024MB) to 4GB (4096MB)**  

## Audio <a name = "audio"><a/>
For this section we only be looking at, **General **and** Global Audio Devices** everything else is for you to learn about.

### General <a name = "audio-General"><a/>
Depending on whatever you're audio devices are on in your PC you may either have go for **44.1kHz** or **48 kHz**

Leave **Channels **to** Stereo**

### Global Audio Devices <a name = "audio-GlobalAudioDevices"><a/>

Select whatever your **Desktop Audio** and **Mic/Auxiliary Audio** are.

## Video <a name = "video"><a/>

Leave **Base (Canvas) Resolution** and **Output (Scaled) Resolution** to whatever they are.  You may have to change it depending on your use case.


**Downscale Filter** can either be **Bicubic** or **Lanczos** 
- **Lanczos** uses more resources but has sharper image quality
- **Bicubic** is a good balance between resource use and and image quality


## Hotkeys <a name = "hotkeys"><a/>
[Include Image of Hotkeys]

Go to the **Hotkeys tab** and scroll until you find **"Start Replay Buffer"** and **"Stop Replay Buffer"**, personally I didn't set these up but you may want to.

Scroll down a little more until you see **Replay Buffer** with only one hotkey available, **"Save Replay"**, choice is your to make it whatever you want.


## Advanced <a name = "advanced"><a/>
Going to be focusing on **General, Video, and Recording.** 

### General <a name = "advanced-General"><a/>
**Process Priority** can be left on either **Normal or Above Normal**
- All this does is prioritize resources for OBS

### Video <a name = "advanced-Video"><a/>
**Renderer** should already be set to **Direct3D 11** but if it isn't then leave it.

Set **Color Format** to **NV12**

Set **Color Space** to **709**

Set **Color Range** to **Partial**

### Recording <a name = "advanced-Recording"><a/>
You can ignore this if you want but it's could be useful to you

**Filename Formatting** basically allows you to change the information presented in the title of the clips, I'll give you the options and customize to your heart's content.

[Insert Image of Filename Formatting Info]

# Debugging <a name = "debugging"><a/>
This part is going to be a major help in fixing problems you may incur on following this guide.  

The way they recommend to debug is 
1. **Run the Replay Buffer for 30s or longer**
	- Optional: **Save Replay**
2. **Stop the Replay Buffer**
[Image Needed of Help>Upload Current Log File]
3. Follow the image and click on **Upload Current Log File**
4. Click **Analyze**
	- This will bring you to a website that displays **Critical Issues, Warnings, and Info**  and will help you debug by stating the problems arising in your case as well as stating solutions to them.  It has also helped me fix some bugs that I found through my journey of this.

> But MFGAVIN, this shit still ain't working!

So if all of this still hasn't worked then I'd like to direct you towards the[OBS Discord Server](https://discord.gg/obsproject) which has support desks.  I left this as the last option since depending on how good this guide does I don't want to overflow the discord with the same shit.



# Making OBS Open on Startup <a name = "obsAutoStart"><a/>

**Thanks to Koala for letting me use this guide they made for here.**

With this guide you will be able to run OBS as an administrator on login without elevation prompt by using the task scheduling feature of Windows.  

You should find the **Task Scheduler** by searching for "task scheduler" in **Windows Search**. It should find your localized name for task scheduler.  
In **Task Scheduler**, right-click the library and select **Create Task**.  
  

![1583868520119.png](https://obsproject.com/forum/attachments/1583868520119-png.51853/ "1583868520119.png")

  
  
Set the properties of the task like this:  

![1583867348367.png](https://obsproject.com/forum/attachments/1583867348367-png.51847/ "1583867348367.png")

  
It's important to **"Turn only when user is logged on"**. If you don't do this, OBS will not appear on the desktop but run only in background.  
Running with admin privileges is activated with **"Run with highest privileges"**.  
  
  

![1583867487846.png](https://obsproject.com/forum/attachments/1583867487846-png.51848/ "1583867487846.png")

  
  

![1583867530864.png](https://obsproject.com/forum/attachments/1583867530864-png.51849/ "1583867530864.png")

  
  
The action in detail:  

![1583867551076.png](https://obsproject.com/forum/attachments/1583867551076-png.51850/ "1583867551076.png")

  
You can add agruments as well such as, **--startreplaybuffer --minimize-to-tray** 
[Click here for the rest of available agruments.](https://obsproject.com/wiki/Launch-Parameters)
 
The **"Start in" directory is important**, you have to s**et it to the directory where obs64.exe is located**. If you don't set it, you get errors that several locale files cannot be found.  

Ex: _C:\Program Files\obs-studio\bin\64bit\\
**Remember to include the dash that's after 64bit to make it work**
  
In the Settings might be of interest to you. **Deactivate "Stop the task if it runs longer than..."** if you never terminate OBS.  

![1583867697595.png](https://obsproject.com/forum/attachments/1583867697595-png.51852/ "1583867697595.png")

  
  
This task scheduler trick works for every app you want to start at login. However, it's kind of a security risk.  
You can even put an icon on the desktop that, upon click, will start this task manually, so you start OBS Studio as administrator without elevation prompt. Create a new shortcut with this target:  
  
C:\Windows\System32\schtasks.exe /run /tn "OBS Studio autostart"  
  
Notice that "OBS Studio autostart" is the name of the scheduled task you gave on the first property page of the task.

# The Guide Itself <a name = "guide"><a/>
This section is purely for the development of the guide itself.
Also it's WIP cuz Idk what to put it in rn

# Credits & Cited Sources <a name = "citations"><a/>
I'd like to give thanks to the [OBS discord server](https://discord.gg/obsproject) and [Epos Vox's discord server](https://discord.gg/eposvox) for helping with questions I had.

Then thanks to [StuckInLimbo's OBS-ReplayBuffer-Setup](https://github.com/StuckInLimbo/OBS-ReplayBuffer-Setup) as I heavily used the information provided to make this guide

And lastly, thanks to OBS User, Koala for letting me use [their guide](https://obsproject.com/forum/threads/start-obs-as-administrator-on-startup-in-windows-10-with-startreplaybuffer.116313/) on how to make OBS Startup in Administrator mode using Task Scheduler.  
