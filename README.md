### @RedBrumbler#6295 ‘s (or u/RedBrumbler) and @Rugtveit#1337 ‘s Guide to making custom sabers for the BeatOn Asset replacement mod


required programs/files for making a saber:
------
- Unity version [2018.3.10f1](https://unity3d.com/get-unity/download?thank-you=update&download_nid=61246&os=Win)
- The unity project from [this tutorial](https://bs.assistant.moe/Sabers/)

![alt text](https://github.com/RedBrumbler/BeatOnCustomSabers/blob/master/Guide%20files/unityprojectDL.png)
- Model program of your choice (RedBrumbler prefers fusion360)
- UnityAssetBundleExtractor [(UABE)](https://mega.nz/#!eRY3gAAI!wEB5cTEAxtEEbe7jIKroatUxwYtwmcUnCjAzoMBEyCs)
NOT our program, be careful when downloading programs from the internet!
- http://www.meshconvert.com/
- The [Guide Files.zip](https://github.com/RedBrumbler/BeatOnCustomSabers/raw/master/Guide%20files/Guide%20files.zip) Contains an .stl SaberTemplate, .obj SaberTemplate and a configured beatonmod.json


Splitting pre-made models:
------
Video for this coming soon!

Making your own models:
------
You can also make your own models!
I will not make this guide on how to use model software to do so, just how to export the files from your model program to something usable for making the sabers, 
make sure to have the different parts split up to make sure you can give them the different textures/shaders
For example, this sword I made is split into different parts:

![alt text](https://github.com/RedBrumbler/BeatOnCustomSabers/blob/master/Guide%20files/SwordBlade.png)

The blade and shiny accents

![alt text](https://github.com/RedBrumbler/BeatOnCustomSabers/blob/master/Guide%20files/shinyaccent.png)

The slightly colored white bits

![alt text](https://github.com/RedBrumbler/BeatOnCustomSabers/blob/master/Guide%20files/Handle.png)

And the handle
Together these make the sword possible:

![alt text](https://github.com/RedBrumbler/BeatOnCustomSabers/blob/master/Guide%20files/Sword.png)

Meshes don’t have to be connected to function as one mesh! so whatever you do, if you have multiple meshes that need to be one, export them as one file, otherwise you won’t be able to get them into the mod correctly.

Please keep in mind that before you export, you should resize and orient the saber to the provided SaberTemplate. Move YOUR saber, not the template! this makes sure that we get the sword in the right position. Make sure that the “top” (non-cutting side) of your sword is aligned with the arrow on the template (from the [Guide Files.zip](https://github.com/RedBrumbler/BeatOnCustomSabers/raw/master/Guide%20files/Guide%20files.zip)), and that the sword is aligned with the template along it's length 

![alt text](https://github.com/RedBrumbler/BeatOnCustomSabers/blob/master/Guide%20files/Template.png)

export the 3 files seperately, preferably as a .obj file, but if you’re like me and use fusion360 or other program that can’t export as .obj, you’ll have to convert the mesh format to .obj using http://www.meshconvert.com/


Getting them into a mod:
====== 
After getting your .obj files you’ll be able to make them into a mod compatible with Beat saber for quest

You’ll start by installing unity version 2018.3.10f1 and opening the unity project that you have downloaded (see required files) it might say you opened it with the wrong unity version but that is okay since it should port over fine since we’re only using the project for reference and to make sure that the sabers are the correct size


open the unity project by double clicking on sabers.unity

![alt text](https://github.com/RedBrumbler/BeatOnCustomSabers/blob/master/Guide%20files/modfiles1.png)

Move in the seperate .obj files

![alt text](https://github.com/RedBrumbler/BeatOnCustomSabers/blob/master/Guide%20files/modfiles2.png)

To check if they are oriented correctly, move them into the left field

![alt text](https://github.com/RedBrumbler/BeatOnCustomSabers/blob/master/Guide%20files/modfilesmissing.png)

If you look at the sword, it should be facing down, and what you want to be the upside to be in beat saber should be pointing in the direction of the sabers which are there, and the handle should be sticking up somewhat on top of them (just like in the image)

If the orientation is not correct you need to go back to your model software and change the placement and orientation of your models in there, and then save them and get them in unity again DELETE THE OLD MODELS FROM UNITY, THEY’LL ONLY MAKE THE NEXT STEP HARDER (if orientation is correct of course don't delete the models)

Raw Unity Mesh Files
------
Now that your orientation is right it’s time to convert them into raw unity mesh files
To start off with that, you’ll need to build the scene, press Ctrl + shift + b to open build settings, and build the scene for windows, mac and linux

![alt text](https://github.com/RedBrumbler/BeatOnCustomSabers/blob/master/Guide%20files/modfiles3.png)

let it build in a folder of your choice, and open UABE

![alt text](https://github.com/RedBrumbler/BeatOnCustomSabers/blob/master/Guide%20files/modfilesmissing2.png)

once in UABE, go to file -> open and navigate to the folder you built the scene in, for me it’s called build
Inside the build folder should be a folder called customSabers_data, go into that folder and open sharedassets0.assets with UABE

![alt text](https://github.com/RedBrumbler/BeatOnCustomSabers/blob/master/Guide%20files/modfiles4.png)

You’ll get this screen, and your models will have a name, to know which is which you can look at the sizes, for example the size of the handle was the largest, so we know that the largest file here is the handle mesh. looking at the sizes before you make the raw files and after can help you identify them. To get the raw unity mesh data you click on export Raw and you’ll have to save the file as a name.
name the blade mesh SaberBlade.dat, name the handle mesh SaberHandle.dat and name the accents SaberGlowingEdges.dat

![alt text](https://github.com/RedBrumbler/BeatOnCustomSabers/blob/master/Guide%20files/modfiles5.png)

put these files in a folder that makes sense to you
I put them in here, with the beatonmod.json

![alt text](https://github.com/RedBrumbler/BeatOnCustomSabers/blob/master/Guide%20files/modfiles6.png)

Now to make the actual mod, if you haven’t already download the [Guide Files.zip](https://github.com/RedBrumbler/BeatOnCustomSabers/raw/master/Guide%20files/Guide%20files.zip) and open the beatonmod.json in a text editor (would not recommend regular notepad, something like notepad++ works way better)

![alt text](https://github.com/RedBrumbler/BeatOnCustomSabers/blob/master/Guide%20files/modfiles7.png)

at the top of the json you’ll see this info, now all you have to do is input your own info in there and name things correctly.
We recommend to only change the id, name, author, description and version numbers

for my sword I changed it to this:

![alt text](https://github.com/RedBrumbler/BeatOnCustomSabers/blob/master/Guide%20files/modfiles8.png)

Now that you have all your files ready you can bundle them into a zip file (winrar or 7zip work fine for this) make sure your zip file contains:
- beatonmod.json
- SaberBlade.dat
- SaberHandle.dat
- SaberGlowingEdges.dat

Now you should be ready to upload to BeatOn!

![alt text](https://github.com/RedBrumbler/BeatOnCustomSabers/blob/master/Guide%20files/modfiles9.png)

If it doesn’t work you might have to reset your assets (will lose all loaded songs, be careful!) but pressing reload songs will load back most of them, if it says invalid mod file you might miss some files or made an incomplete json




