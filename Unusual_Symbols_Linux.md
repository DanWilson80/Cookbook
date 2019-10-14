Using Unusual Symbols in Linux
======

Index  
[Using Unicode](#Unicode)  
[Using Emojis](#Emojis)  

Unicode
------
### Useful Resources for Using Unicode with Unix system  
  
#### GNOME DESKTOP  
**Gucharmap character map is a part of GNOME desktop. So if you run a Gnome desktop - you can access it in following way:**
  * Menu on the top of the screen. Click on chosen language ➢ choose Character Map.
  * gucharmap in terminal.
  * Applications ➢ Accessories ➢ Character Map.  
---
* [Gucharmap Homepage](https://wiki.gnome.org/action/show/Apps/Gucharmap?action=show&redirect=Gucharmap) on Gnome.org.  
* [Character Map information](https://help.ubuntu.com/community/CharacterMap) on Ubuntu.com.  
* [Compose Key Info for Ubuntu](https://help.ubuntu.com/community/ComposeKey)  
* [Linux keyboard shortcuts for text symbols](https://fsymbols.com/keyboard/linux/)  
* [ALT Keys and Linux](https://www.linux.org/threads/alt-keys-and-linux.11517/)  
---
[Unicode Chart](https://unicode.org/charts/)  
This [page](https://www.alt-codes.net/arrow_alt_codes.php) has Alt-Key Codes at the top (which are Windows only) but scroll down for Unicode Hex of different arrows.  
It also has a list of other Code resources on the right hand side of the page for many other symbols. 
[Unicode Blog](https://www.alt-codes.net/blog/unicodes-10%22;)  
[Character Maps](https://fsymbols.com/character-maps/)    
[Symbols](https://fsymbols.com/) - Copy and Paste. Includes Emojis, Emoticons, Facebook and Text Art.  
[Facebook Symbols](https://fsymbols.com/) - Copy and Paste.   


  
### How to Type A Special Character Using Unicode Hex  
* Some characters require a "Compose Key"  
* This can be bound using **Gnome-Tweak**, if you need to install it use:
```
sudo apt install gnome-tweaks

gnome-tweaks (opens interface after installation)
```  
* Go to "Keyboard & Mouse" section. The "Compose Key" options is disabled by default. Click on the "Disabled" button.
* This will bring up a Dialog Box with a range of options of key to use I have mine bound to my `Right ALT` key.

##### Entering a Unicode Hex
* To enter the code just hold `Shift + CTRL and press u` this will change your cursor to a litle "u"
* **Type** the Unicode Hex for your desired character or symbol then press `Enter` to display the symbol.  
  
[Index](#Index)  
---  
  
Emojis
------
Note that this only works in GTK apps, so applications like Firefox, Google Chrome, and LibreOffice will not offer it. Bummer, but can always copy-paste emoji from Gedit I suppose.  
* In Ubuntu 18.04 all native text editing software now has an emoji picker, and it’s not hard to find: you can right-click in any text field and click “Insert Emoji.”  
* Alternatively you can use the keyboard shortcut Ctrl+. to trigger the window directly and find an appropriate emoji for what you’re trying to say.  
  
### Installing an Emoji Keyboard  
  
`sudo apt install ibus`

* IBus works by installing different modules for different languages. In this case, you’ll need UniEmoji to allow it to type out emoticons. You’ll need to install it from source to get things working. This is easy enough to do with these commands:  
  
```
sudo add-apt-repository universe && sudo apt update
sudo apt install git make
git clone https://github.com/salty-horse/ibus-uniemoji.git
cd ibus-uniemoji
sudo make install
ibus restart
```   
* This should install everything you need to get emoticons working with IBus, finally restarting the program if it’s running (so it can see the new module). If you find that the program isn’t working properly, try installing these prerequisites:  
  
`sudo apt install python gir1.2-ibus-1.0`  
  
* These are two pieces of software that UniEmoji relies on to work. They’re usually included by default in Ubuntu, so you shouldn’t have to do this. If you want, you can also install a piece of software which will make searching up emojis faster, using these commands:  
  
```
sudo add-apt-repository universe && sudo apt update
sudo apt install python-levenshtein
```  
  
* The first line is only needed if the second line doesn’t work. That is to say, if APT can’t find the package you’re looking for.  
  
###Setting Up  
* Once you’ve done this, you’ll need to do some extra setup to make things work properly. After installing a language, IBus needs to add it as an active input method. In this case, you’ll need to add UniEmoji first.

Your steps will be slightly easier if you use the GNOME desktop, since it integrates IBus in its system. If you followed the instructions above, all you need to do is open up your system settings, and navigate to the relevant place. Do this by entering in the command below:  
  
`gnome-control-center`  
  
* From there, go to Region & Language > Input Sources. You should see an option to add new sources (the plus button). Select this, and click on the More button (the stack of three squares at the bottom). From here, click on Other > Other (uniemoji). You should be able to select this by double clicking, or selecting the Add button.  
  
* You’ll know if the steps worked or not if you can click on the IBus tray icon. UniEmoji should be an option for you to select. By default, you can also switch to it by pressing the Super + Space keys.  
  
### Emoji Input: Mouse
* If you’d prefer to select your emojis by mouse, there’s an easy solution called Emoji Keyboard. It resides in your system tray as a panel you can show and hide, which provides you with a way to copy or insert the emoji of your choice.  

* Getting it is quite easy if you’re using a Debian-based Linux operating system. All you need to do is head to the program’s Github page and install the provided DEB file. This should be as easy as double clicking it. Any required programs should be installed along with it, no other steps required. If this is not the case, you may have to run these commands below first, which should fix these problems:  
  
```
sudo add-apt-repository universe && sudo apt update
sudo apt install xclip
```
  
From here, you should be able to launch the program from your application menu (or from the terminal using the command emoji-keyboard). This should create an icon in your system tray. You can click on this, to bring up a set of options, including settings to adjust its behavior, and a virtual keyboard to enter emojis.  
  
`emoji-keyboard`  
  
* On future reboots, you shouldn’t have to worry about manually starting the program. By default, it will run on startup.  
  
[Index](#Index)


