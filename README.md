### @RedBrumbler#6295 ‘s (or u/RedBrumbler) Guide to making custom sabers for the BeatOn Asset replacement mod

**CoEdited by Yuuki#0802**

(Rugtveit has withdrawn from the guidemaking so their name has been taken out)

#### DISCLAIMER: Making custom sabers / getting custom sabers to work may require you to reset your assets (thus making you sort your songs again) multiple times, so losing all your song data is not uncommon, I am not responsible for you needing to reset your assets so don't complain about it to me

## Table of Contents:

1. [Useful Links](##useful-links)
2. [Required Programs/Files](##required-programs/files-for-making-a-saber)
3. [Get Your Saber Model](#get-your-saber-model)
4. [Converting Your Objects to a Mod](#converting-your-objects-to-a-mod)

Useful links:
------
- [BeatOn by Emulamer](https://github.com/emulamer/BeatOn/releases)
- [Sidequest Discord](https://discord.me/sidequestvr)
- [Fusion360](https://www.autodesk.com/products/fusion-360/students-teachers-educators)
- [Blender](https://www.blender.org/)
- [Custom Sabers]()
- [Custom Blocks/Notes]()
- [Other Asset Mods]()

Required Programs/Files for Making a Saber:
------
- Unity version [2018.3.10f1](https://unity3d.com/get-unity/download?thank-you=update&download_nid=61246&os=Win) or higher (any lower and BeatSaber will crash)
- This [unity project](https://bs.assistant.moe/Sabers/resources/CustomSaberUnityProject.zip). Source: [here](https://bs.assistant.moe/Sabers/)
- Model program of your choice (I prefer fusion360)
- UnityAssetBundleExtractor [(UABE)](https://mega.nz/#!eRY3gAAI!wEB5cTEAxtEEbe7jIKroatUxwYtwmcUnCjAzoMBEyCs)
  *NOT my program, be careful when downloading programs from the internet!*
- The [Guide Files.zip](https://github.com/RedBrumbler/BeatOnCustomSabers/raw/master/Guide%20files/Guide%20files.zip) Contains an .stl SaberTemplate, .obj SaberTemplate and a configured beatonmod.json

# Get Your Saber Model


Splitting pre-made models:
------
#### [Separating Objects in Blender](https://youtu.be/P_C3xkVT044)

Converting PC .saber files:
------
Rule established by the BSMG around porting sabers:

>Right now, we decided the rule for porting sabers is that the port has to 100% say the original author, but you can get a "porter" credit. If a certain author doesn't want their models ported for some reason, they can "opt out" from that ever happening. If the model changes much from how the original author intended it, the porter would need to get permission from the original creator and possible joint authorship can happen then.
>
>We decided to do it this way because if we ever 100% automate the process of using PC sabers, there'd be no question of whether you could use a saber made for Beat Saber. Requiring explicit permission on a port would slow down ports I think and with the author still getting credit, the modelers when asked didn't seem to have an issue with it. We'll let you know if any of that changes! (just PM if any modeler has an issue with this policy)

**Short Version:**

1. Download desired saber from [ModelSaber](https://modelsaber.com/)
2. Open .saber file with UABE
3. Click Export
4. Click Info
5. Click plugins in UABE and save the meshes as .obj
6. Open all .obj files in modeling program
7. Orient meshes to match saber template
8. Export to the three required .obj (Blade.obj, Handle.obj, GlowingEdges.obj)
9. Skip to ["Getting Them Into a Mod"]()


Making your own models:
------
You can also make your own models!

I will not make this guide on how to use model software to do so, just how to export the files from your model program to something usable for making the sabers, make sure to have the different parts split up to make sure you can give them the different textures/shaders.

For example, this sword I made is split into different parts:

![alt text](https://github.com/RedBrumbler/BeatOnCustomSabers/blob/master/Guide%20files/SwordBlade.png)

The blade and shiny accents. Saved this part as `Blade.obj`

![alt text](https://github.com/RedBrumbler/BeatOnCustomSabers/blob/master/Guide%20files/shinyaccent.png)

The slightly colored white bits. Saved this part as `GlowingEdges.obj`

![alt text](https://github.com/RedBrumbler/BeatOnCustomSabers/blob/master/Guide%20files/Handle.png)

And the handle. Saved this part as `Handle.obj`

Together these make the sword possible:

![alt text](https://github.com/RedBrumbler/BeatOnCustomSabers/blob/master/Guide%20files/Sword.png)

Meshes don’t have to be connected to function as one mesh! So, whatever you do, if you have multiple meshes that need to be one, export them as one file, otherwise you won’t be able to get them into the mod correctly.

Please keep in mind that before you export, you should resize and orient the saber to the provided SaberTemplate. Move YOUR saber, not the template! This makes sure that we get the sword in the right position. Make sure that the “top” (non-cutting side) of your sword is aligned with the arrow on the template (from the [Guide Files.zip](https://github.com/RedBrumbler/BeatOnCustomSabers/raw/master/Guide%20files/Guide%20files.zip)), and that the sword is aligned with the template along it's length 

#### I have created a new Model Template, it's way clearer to use and will let you orient the sword correctly no doubt! It also contains some tips on where to put different parts when you are modeling your own sabers (like thickness, where to start the blade, and where to place the hilt and pommel)

![alt text](https://github.com/RedBrumbler/BeatOnCustomSabers/blob/master/Guide%20files/Template.png)

export the 3 files separately, preferably as a .obj file, but if you’re like me and use fusion360 or other program that can’t export as .obj, you’ll have to convert the mesh format to .obj using http://www.meshconvert.com/



#### Note: In order to use your Saber on BeatOn, you **MUST** have three separate pieces. Each piece represents a different material used in game (like so):

![alt text](https://github.com/RedBrumbler/BeatOnCustomSabers/blob/master/Guide%20files/example-saber.jpg)
![alt text](https://github.com/RedBrumbler/BeatOnCustomSabers/blob/master/Guide%20files/model-example.png)

It is also possible for you to have dummy pieces instead of having three separate objects. For example, you can have just a blade and handle and for the glowing edges, you can add an extra mesh hidden inside your model.

![alt text](https://github.com/RedBrumbler/BeatOnCustomSabers/blob/master/Guide%20files/dummy-piece.png)

Converting Your Objects to a Mod:
====== 
After getting your .obj files, you’ll be able to make them into a mod compatible with Beat Saber for Quest

You’ll start by installing unity version 2018.3.10f1 and opening the unity project that you have downloaded (see required files). It might say you opened it with the wrong unity version but that is okay since it should port over fine since we’re only using the project for reference and to make sure that the sabers are the correct size.


Open the unity project by double clicking on sabers.unity

![alt text](https://github.com/RedBrumbler/BeatOnCustomSabers/blob/master/Guide%20files/modfiles1.png)

Move in the separate .obj files

![alt text](https://github.com/RedBrumbler/BeatOnCustomSabers/blob/master/Guide%20files/modfiles2.png)

To check if they are oriented correctly, move them into the left field

![alt text](https://github.com/RedBrumbler/BeatOnCustomSabers/blob/master/Guide%20files/modfilesmissing.png)

If you look at the sword, it should be facing down, and what you want to be the upside to be in Beat Saber should be pointing in the direction of the sabers which are there, and the handle should be sticking up somewhat on top of them (just like in the image)

If the orientation is not correct you need to go back to your model software and change the placement and orientation of your models in there, and then save them and get them in unity again. DELETE THE OLD MODELS FROM UNITY, THEY’LL ONLY MAKE THE NEXT STEP HARDER (if orientation is correct, of course, don't delete the models)

Raw Unity Mesh Files
------
Now that your orientation is right it’s time to convert them into raw unity mesh files. To start off with that, you’ll need to build the scene, press Ctrl + shift + b to open build settings, and build the scene for windows, mac and linux

![alt text](https://github.com/RedBrumbler/BeatOnCustomSabers/blob/master/Guide%20files/modfiles3.png)

Let it build in a folder of your choice (I would create a new folder called "Build") and open UABE

![alt text](https://github.com/RedBrumbler/BeatOnCustomSabers/blob/master/Guide%20files/modfilesmissing2.png)

Once in UABE, go to file -> open and navigate to the folder you built the scene in.

Inside the build folder should be a folder called customSabers_data, go into that folder and open sharedassets0.assets with UABE

![alt text](https://github.com/RedBrumbler/BeatOnCustomSabers/blob/master/Guide%20files/modfiles4.png)

You’ll get this screen, and your models will have a name, to know which is which you can look at the sizes, for example the size of the handle was the largest, so we know that the largest file here is the handle mesh. Looking at the sizes before you make the raw files and after can help you identify them. To get the raw unity mesh data you click on export Raw.

*Remember earlier: we named each object based on the material we wanted them to have. This is important now as well. Ex. `Blade.obj` should become `SaberBlade.dat`. `Handle.obj` should become `SaberHandle.dat`. GlowingEdges.obj should become `SaberGlowingEdges.dat`*

![alt text](https://github.com/RedBrumbler/BeatOnCustomSabers/blob/master/Guide%20files/modfiles5.png)

Put these files in a new folder that is the name of your saber (we will be converting this folder to .zip for easy uploading later)

![alt text](https://github.com/RedBrumbler/BeatOnCustomSabers/blob/master/Guide%20files/modfiles6.png)

Now to make the actual mod, if you haven’t already download the [Guide Files.zip](https://github.com/RedBrumbler/BeatOnCustomSabers/raw/master/Guide%20files/Guide%20files.zip) and open the beatonmod.json in a text editor (would not recommend regular notepad, something like notepad++ works way better)

#### A new update to Beaton (0.9.8) Brought us the possibility of adding cover images to our mods, it doesn't matter too much what the image is (make it recognizable! for sabers I recommend using a picture of the saber, look at my saber pictures/mod Cover images for a way to do this!) just make sure the image is 150 (w) x 200 (h) and is named "Cover.png" that way it will show up in BeatOn

At the top of the json you’ll see this info, now all you have to do is input your own info in there and name things correctly.
I recommend to only change the id, name, author, description and version numbers

```
"id": "ModID",
  "name": "Mod name",
  "author": "YourName",
  "description": ["Mod Description"],
  "gameVersion": "1.1.0",
  "version": "1.0.0.0",
  "platform": "Quest",
  "category": "Saber",
  "coverImageFilename": "Cover.png",
  "components":
```

for my sword I changed it to this:

```
"id": "ConnieSwordV1", --Unique mod ID, this makes sure that when you release an update it won't install the mod again, but overwrite the old one
  "name": "Connie's Sword V1", --The name displayed within BeatOn
  "author": "RedBrumbler", --Your name here, so people know who made that saber
  "description": ["Connie's sword Bismuth made for her from the Cartoon Network Show 'Steven Universe'"], --description, can be used to credit others whose work you worked off of, or a great place to make meta jokes
  "gameVersion": "1.1.0",
  "version": "1.0.1.0", --Version of the mod, I reccommend to bump the last number up for small changes, but for larger redesigns use the second number
  "platform": "Quest",
  "category": "Saber",
  "coverImageFilename": "Cover.png", --it's easier to just name the cover image to Cover.png than to keep editing this one IMO -Redbrumbler
  "components":
```



Now that you have all your files ready you can bundle them into a zip file (winrar or 7zip work fine for this) make sure your zip file contains:
- beatonmod.json
- SaberBlade.dat
- SaberHandle.dat
- SaberGlowingEdges.dat
- Cover.png

#### A .rar file won't work! It has to be .zip!

Now you should be ready to upload to BeatOn!

![alt text](https://github.com/RedBrumbler/BeatOnCustomSabers/blob/master/Guide%20files/modfiles9.png)

If you get "invalid mod", you likely are missing an argument in the info part I just listed, make sure all of it is there!

If it doesn’t work you might have to reset your assets (will lose all loaded songs, be careful!) but pressing reload songs will load back most of them, if it says invalid mod file you might miss some files or made an incomplete json

If sabers (even confirmed working ones) don't show up at all then you might even need to completely reinstall beat saber

I also support adding your sabers to the repository here!
(explanation adapted from @Yuuki#0802 from BSMG, and by that I mean mostly blatantly copied)
1. Make a Github account if you haven't already
2. Click the "fork" button in the top right of this repository
3. Download [github desktop](https://desktop.github.com/)
4. Go to your forked repo (so, yourname/BeatOnCustomSabers) and click "Clone or Download", Copy that link
5. Go to Github Desktop: File -> Clone repository -> URL and paste the link, then click clone (keep note of the local path you put the repo in)
6. Head to where you saved the repo in your file explorer (C:\User\GitHub\BeatOnCustomSabers)
7. Go to the "Sabers" folder.
8. Create a new folder for your sabers (ex. "LaBandit915's sabers")
9. Drag your zip file in this folder
10. Head back to Github desktop
11. Add a summary for your commit at the bottom left (ex. "Added {saberName} by LaBandit915")
12. Press commit
13. Press push
14. Go back to your forked repo and press "Create pull request" and submit!

***Once I or Yuuki accepts your pull request your saber will be added here!***