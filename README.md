### qbox-klipperscreen

##### [KlipperScreen](https://github.com/KlipperScreen/KlipperScreen) configuration to add controls for the QiDi Box.



These configuration files allow you to add a button to the home screen of KlipperScreen that brings up a new windows with controls to Remove and Reload the four filaments in your QiDi Box. The [q2-wiki repository at qidi-community](https://github.com/qidi-community/q2-wiki/blob/main/content/klipperscreen-installation/README.md) has instructions on installing KlipperScreen on your QiDi Q2.

**I apologize for the craptasic screenshots**

##### The main screen

![alt main screen](https://github.com/RickSeiden/qbox-klipperscreen/blob/25d5bf51f21cafbbe9e4d73d19dcf70b804a10c3/screenshots/main_screen.jpg)

##### The "box" screen

![alt box screen](https://github.com/RickSeiden/qbox-klipperscreen/blob/25d5bf51f21cafbbe9e4d73d19dcf70b804a10c3/screenshots/qidi_screen.jpg)

#### Installing this configuration



1. Download the logo_qidi_white.svg file and copy it to \~/KlipperScreen/styles/<your\_style>/images

   a. There are a few folders under styles, and I wasn't sure which one was being used, so I copied it into all the images directories, just to be safe
2. In Fluidd, open the Configuration window and open the KilpperScreen.conf file

   a. You should back this up by SSHing into your printer and creating a copy, but the file has a "Do not edit below this line" warning at the top.  All your edits will go above that line, and if you delete everything above the line, it will restore your original file.
3. Above the first line (that "Do not edit above this line") add the contents of KlipperScreen.conf in this repository and save your changes
4. Restart KlipperScreen using one of these methods

   a. Power cycle the printer
   b. In SSH issue the command
    sudo service KlipperScreen restart



You should now have a QiDi logo with QiDi box under it, and tapping it will bring you to a screen with two rows of four buttons that let you Remove or Reload each spot in the box.


#### Edits to Python files

**Remember to make backups of all files before you edit them!**

* [KlipperScreen/ks_includes/files.py](https://github.com/RickSeiden/qbox-klipperscreen/blob/1936e719810bab886a4d5c42b52de8bfdd7f3fb3/files.py_changes.md)
* [KlipperScreen/panels/gcodes.py](https://github.com/RickSeiden/qbox-klipperscreen/blob/fa0b1ccffe724718f972a84c3a86803a9f350c87/gcodes.py_changes.md)

#### Disclaimer

You know what's coming here.  While this is a small and fairly straight forward change, you are making these changes at your own risk. I cannot be responsible for anything that happens to your printer.  Period.  You're 100% on your own if you try to do this. I can't offer more support than what you see here, and if something goes South, all I can say is to revert KlipperScreen.conf.



##### License

The text in the KlipperScreen.conf file is my original work and is considered in the public domain.
The QiDi logo in logo_qidi_white.svg is Copyright QiDi Technologies.  They reserve all rights.





