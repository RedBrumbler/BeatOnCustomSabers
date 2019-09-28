# Guide to Making Custom Bombs for BeatOn

###  iplay games!#8247‘s (or Futuremappermydud) Guide to making custom bombs for the BeatOn Asset replacement mod

#### DISCLAIMER: Making custom bombs / getting custom bombs to work may require you to reset your assets (thus making you sort your songs again) multiple times, so losing all your song data is not uncommon, I am not responsible for you needing to reset your assets so don't complain about it to me or else

# Table of Contents

1. [Useful Links](#useful-links)
2. [Required Programs/Files](#required-programs-and-files-for-making-a-bomb)
3. [Get Your bomb Model](#get-your-bomb-model)
4. [Converting Your Objects to a Mod](#converting-your-objects-to-a-mod)
5. [Add Your bombs to the Repo](#add-your-bombs-to-the-repo)

# Other guides by me:
# Useful Links and stuff

- [BeatOn by Emulamer](https://github.com/emulamer/BeatOn/releases)
- [Sidequest Discord](https://discord.me/sidequestvr)
- [Beat Saber Modding Group Discord (BSMG)](https://discord.gg/beatsabermods)
- [Fusion360](https://www.autodesk.com/products/fusion-360/students-teachers-educators)
- [Blender(best choice)](https://www.blender.org/)
- [Custom Sabers](https://github.com/RedBrumbler/BeatOnCustomSabers/tree/master/Sabers)
- [Custom Blocks/Notes](https://github.com/RedBrumbler/BeatOnCustomSabers/tree/master/NoteCubes)
- [Other Asset Mods](https://github.com/RedBrumbler/BeatOnCustomSabers/tree/master/MiscAssetMods)

# Required Programs and Files for Making a bomb:

- Unity version [2018.3/4.10f1](https://unity3d.com/get-unity/download?thank-you=update&download_nid=61246&os=Win) or higher (any lower and BeatSaber will crash)
- Model program of your choice (I prefer blender, but RedBrumbler is wierd and likes Fusion360)
- UnityAssetBundleExtractor [(UABE)](https://mega.nz/#!eRY3gAAI!wEB5cTEAxtEEbe7jIKroatUxwYtwmcUnCjAzoMBEyCs)
  *NOT my program, be careful when downloading programs from the internet!*
- The [Guide Files.zip]() Contains an .blend with examples for modeling,obj of retro note example, and a beatonmod.json
# Get Your bomb Model
Making your own model:
------

You can also make your own model!

I will not make this guide on how to use model software to do so, just how to export the files from your model program to something usable for making the sabers, make sure to have the different parts split up to make sure you can give them the different textures/shaders.

For example, this bomb I made is based on a retro feel:

![alt text](https://github.com/Futuremappermydud/BeatOnCustomSabers/blob/master/Guidefiles/GuideFiles%20Bomb/0.01%20retro%20preview.PNG)

once you have your model

![alt text](https://github.com/Futuremappermydud/BeatOnCustomSabers/blob/master/Guidefiles/GuideFiles%20Bomb/0.1%20model%20preview.PNG)

you want to create a folder you will remember

![alt text](https://github.com/Futuremappermydud/BeatOnCustomSabers/blob/master/Guidefiles/GuideFiles%20Bomb/0.2%20create%20memorable%20folder.PNG)

Next export the model to this folder as bomb.obj

![alt text](https://github.com/Futuremappermydud/BeatOnCustomSabers/blob/master/Guidefiles/GuideFiles%20Bomb/0.3%20export%20to%20folder%20as%20bomb.obj'.PNG)

Converting Your objects into a mod
====== 
After getting your .obj file, you’ll be able to make them into a mod compatible with Beat Saber for Quest

You’ll start by installing unity version 2018.3/4.10f1 and create a new project


Open that unity project so we can begin

![alt text](https://github.com/RedBrumbler/BeatOnCustomSabers/blob/master/Guidefiles/modfiles1.png)

Move in the .obj file

![alt text](https://github.com/RedBrumbler/BeatOnCustomSabers/blob/master/Guidefiles/modfiles2.png)

So we can build the bomb (AKA, compile [i think]), move them into the left field of unity

![alt text](https://github.com/RedBrumbler/BeatOnCustomSabers/blob/master/Guidefiles/modfilesmissing.png)

Raw Unity Mesh Files
------
Now that your bomb is in unity, it’s time to convert them into raw unity mesh files. To start off with that, you’ll need to build the scene, press Ctrl + shift + b to open build settings, and build the scene for windows, mac and linux

![alt text](https://github.com/RedBrumbler/BeatOnCustomSabers/blob/master/Guidefiles/modfiles3.png)

Let it build in a folder of your choice (I would create a new folder called "Build") and open UABE

![alt text](https://github.com/RedBrumbler/BeatOnCustomSabers/blob/master/Guidefiles/modfilesmissing2.png)

Once in UABE, go to file -> open and navigate to the folder you built the scene in.

Inside the build folder should be a folder called customSabers_data, go into that folder and open sharedassets0.assets with UABE

![alt text](https://github.com/RedBrumbler/BeatOnCustomSabers/blob/master/Guidefiles/modfiles4.png)

You’ll get this screen, and your model will have a name, lol the name is default btw
click the mesh default and click export raw

![alt text](https://github.com/RedBrumbler/BeatOnCustomSabers/blob/master/Guidefiles/modfiles5.png)

Put this raw .dat file in a new folder that is the name of your saber (we will be converting this folder to .zip for easy uploading later)

![alt text](https://github.com/RedBrumbler/BeatOnCustomSabers/blob/master/Guidefiles/modfiles6.png)

Now to make the actual mod, if you haven’t already download the [Guide Files.zip](https://github.com/RedBrumbler/BeatOnCustomSabers/raw/master/Guidefiles/Guidefiles.zip) and open the beatonmod.json in a text editor (would not recommend regular notepad, something like notepad++ works way better)



### Taking a Picture of Your Saber

#### A new update to Beaton (0.9.8) Brought us the possibility of adding cover images to our mods, it doesn't matter too much what the image is (make it recognizable! for sabers I recommend using a picture of the saber, look at my saber pictures/mod Cover images for a way to do this!) just make sure the image is 150 (w) x 200 (h) and is named "Cover.png" that way it will show up in BeatOn

Before starting, you will need to zip your saber up and drag it onto BeatOn's Upload screen. Make sure your saber is installed.

1. Start Beat Saber (not through BeatOn as this will cause the Quest's screencapture capabilities to not work)
2. Head to the tutorial
3. Go back to the Quest home screen and click "Sharing" at the bottom
4. Click record or capture image
5. **If you want to capture image:** Hold your left saber diagonally across your left eye (close your right eye if necessary)
6. **If you want to record:** Hold your saber diagonally and stop the recording. 
7. Plug your Quest up to your PC
8. Open SideQuest
9. Go to the "Files" tab
10. Head to the Oculus -> Screenshots folder
11. Export to your saber's folder
12. If you recorded a video, export the video to a location on your pc, open the video and find a good spot to take a screen shot. Save the screenshot in your saber's folder

At the top(or bottom) of the json you’ll see this info, now all you have to do is input your own info in there and name things correctly.
I recommend to only change the id, name, author, description and version numbers

```
"id": "ModID",
  "name": "Mod name",
  "author": "YourName",
  "description": ["Mod Description"],
  "gameVersion": "1.3.0p2",
  "version": "1.0.0.0",
  "platform": "Quest",
  "category": "Saber",
  "coverImageFilename": "Cover.png",
  "components":
```

for my sword I changed it to this:

```
"id": "retrobombv1", 
  "name": "Connie's Sword V1",
  "author": "RedBrumbler", 
  "description": ["Retro Bomb innovation"], 
  "gameVersion": "1.1.0",
  "version": "1.0.1.0", 
  "platform": "Quest",
  "category": "Saber",
  "coverImageFilename": 
  "components":
```



Now that you have all your files ready you can bundle them into a zip file (winrar or 7zip work fine for this) make sure your zip file contains:
- beatonmod.json
- bomb.dat
- Cover.png(not needed to upload)

#### A .rar file won't work! It has to be .zip!

Now you should be ready to upload to BeatOn!

![alt text](https://github.com/RedBrumbler/BeatOnCustomSabers/blob/master/Guidefiles/modfiles9.png)

If you get "invalid mod", you likely are missing an argument in the info part I just listed, make sure all of it is there!

If it doesn’t work you might have to reset your assets (will lose all loaded songs, be careful!) but pressing reload songs will load back most of them, if it says invalid mod file you might miss some files or made an incomplete json

If sabers (even confirmed working ones) don't show up at all then you might even need to completely reinstall beat saber

# Add Your Bombs to the Repo

I also support adding your bombs to the repository here!
(explanation adapted from @Yuuki#0802 from BSMG, and by that RedBrumbler means mostly blatantly copied)

1. Make a Github account if you haven't already
2. Click the "fork" button in the top right of this repository
3. Download [github desktop](https://desktop.github.com/)
4. Go to your forked repo (so, yourname/BeatOnCustomSabers) and click "Clone or Download", Copy that link
5. Go to Github Desktop: File -> Clone repository -> URL and paste the link, then click clone (keep note of the local path you put the repo in)
6. Head to where you saved the repo in your file explorer (C:\User\GitHub\BeatOnCustomSabers)
7. Go to the "NoteBombs" folder.
8. Create a new folder for your bombs (ex. "LaBandit915's bombs")
9. Drag your zip file in this folder
10. Head back to Github desktop
11. Add a summary for your commit at the bottom left (ex. "Added {BombName} by LaBandit915")
12. Press commit
13. Press push
14. Go back to your forked repo and press "Create pull request" and submit!

***Once RedBrumbler or Yuuki accepts your pull request your bomb(s) will be added here!***

**Please test your mods before submitting. Make sure they have correct JSON formatting and appear correctly on the BeatOn mod screen.**
