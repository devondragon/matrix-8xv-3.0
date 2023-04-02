#Help with converting gifs to be used on your Matrix keyboard screen

The Matrix Eye has a small screen on the right edge which you can load a custom animation into.  The screen is only 60 px by 60 px, so you'll need to pick a video or animated gif that will look good at that size, and cropped to a square aspect ratio.

## Generate a square animated gif file from your source video or animated gif
**1)** First, if you are starting with a video, not an animated gif, you will need to convert the video file to an animated gif.  You can do this for free using this online [Video to GIF converter](https://ezgif.com/video-to-gif)

**2)** Now that you have an animated gif, you will want to crop it to be square.  You don't need to worry about the resolution as we will deal with that in a later step.  You can use this free online [Crop animated GIF Tool](https://ezgif.com/crop)

Choose your animated gif file with the Choose File button, and then click the Upload button.

**3)** Once it's uploaded and shown on the page, make sure you select the "square" aspect ratio under the image.  Then you can adjust the size and position of the crop overlay on the image.  When you have it how you want, click the "Crop Image!" button below.

**4)** It will show the cropped image below.  If it looks good, you can use the "Save" disk icon on the right, under the image.  This will download the square animated gif file to your computer.  You can rename the file to whatever you like.  I recommend making the name short and without any spaces or special characters.  "myfile.gif" is good.  "My super! Cool! File.gif" is bad.  

## Convert the animated GIF into a file the Matrix keyboard can use
Now we need to convert this animated gif into a file format the Matrix keyboard can use.  This requires a few steps on the command line.  I hope to add this as an easy web tool later, but for now...

**1)** Make sure you have [python installed](https://www.python.org/downloads/) on your computer.  

**2)** Then you need to use pip to install numpy and Pillow (version 8.4.0).

On Windows you can run this from the command prompt:
```
py -m pip install numpy
py -m pip install "Pillow==8.4.0"
```

On a Mac run the following from the Terminal:
```
python3 -m pip install numpy
python3 -m pip install "Pillow==8.4.0"
```

**3)** Next, download the [gif2anim.py](scripts/gif2anim.py) python script.  Put it in the same directory as your animated gif file.  This script was written by Astro, so all credit goes to them. I made a minor change to fix an error, but that is it.

**4)** Now run the python script like this, using a gif file named "myfile.gif" as an example:

Windows:
`py ./gif2anim.py "myfile.gif" myfile.sml sml`

Mac:
`python3 ./gif2anim.py "myfile.gif" myfile.sml sml`


The script should run, and create a file called myfile.sml.  This is the file that you will need to load onto the Matrix keyboard in the next portion

## Install the SML file onto your Matrix keyboard
**1)** First we need to mount the SCREEN drive.  Press F24 (by default this is Function + F12).  Your Eye screen will go dark, and a USB drive named SCREEN will be mounted on your computer.  

**2)** Delete (or copy then delete) any old files.  Then copy your new .sml file we created above onto the drive.  When the copy is finished, ejected the drive from the OS.  

**3)** Press F24 again, and your Eye screen should light up and play your new animated image.


