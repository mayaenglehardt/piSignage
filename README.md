## What is PiSignage? 

PiSignage is a very popular Digital Signage Solution primarily used along with Raspberry Pi boards (but can also 
work on other Linux based hardware platforms,for e.g. Intel NUC, see [here](https://pisignage.com/releases/Player2_installation_procedure.html)). 
In addition, piSignage is also available on [Android devices](https://play.google.com/store/apps/details?id=com.pisignage.player2&hl=en&gl=US) and as an [web 
app](https://pisignage.com/player2/)  

All Raspberry Pi models are supported (please use specific image for the various models as mentioned [below](https://github.com/colloqi/piSignage#getting-the-player-ready)).

Raspberry Pi connects to TV through HDMI interface and needs network connectivity to reach pisignage.com or any 
other piSignage server locally configured. 

PiSignage players can be managed centrally using managed services at [pisignage.com](https://pisignage.com) or using a 
separate server using [open sourced server software](https://github.com/colloqi/pisignage-server) or independently using player webUI (http://player-ip:8000).   

**Managing Screens is just a few steps**
 
1. **Upload images/videos**, provide web or streaming links, design and upload HTML assets as a zip file  
2. **Create playlists** by selecting one of the built-in layouts or custom layouts created using the template designer,
   add assets(drag and rearrange for the desired order), enter duration of play for each asset. You can also add a ticker feed and 
   define special playlists for adverts insertion, domination content, lounge music and content play based on events  
3. **Create Groups and assign players** to a group which needs to play the same playlists. Then you can assign and schedule multiple 
    playlists to a group. You can also define display settings, schedule TV on/off and other properties of the group. 
   Whenever ready, Deploy playlists at the 
    click of a button to all the players in the group.  
4. You can **centrally monitor the players** in the dashboard/player screens,view current snapshot of TV, get reports, update software 
    and also issue debug piShell commands.  

**More functions and utilities**

1. You can play/pause playlists, play individual assets from both player and server UIs.
2. Players can operate in kiosk mode pointing to the URL provided and play normal playlists when no key is pressed.
3. Autoconfiguration of players and many such features for bulk management of players.

Please visit [pisignage.com](https://www.pisignage.com) to know more about features and benefits.

## Getting the Player ready
  
  
*Note: By downloading and using piSignage Player software, you agree to our [Terms of Service](https://s3.amazonaws.com/pisignage/legal/piSignage-TOS.html)*  
  
There are 2 ways you can get the piSignage Player Software

<a id="basic"></a>
### Method 1: Download image and Prepare the SD card (minimum 16GB, class 10 or above)

-   [Download PDF Guide - little outdated](https://s3.amazonaws.com/pisignage/pisignage-images/Basic_install.pdf) 

#### Steps to follow
##### 1. Download the complete player iso image  

*For Raspberry Pi high end models like model 5, model 4..*  
   - Use Bookworm OS based **[5.2.1(64bit OS)](https://pisignage.s3.amazonaws.com/pisignage-images/pisignage_5.2.1-64bit.img.zip)** 
        or **[5.2.1(32bit OS)](https://pisignage.s3.amazonaws.com/pisignage-images/pisignage_5.2.1-32bit.img.zip)**  
        Google Drive links **[5.2.1(64bit OS)](https://drive.google.com/file/d/16sI_PNgELZxKLF-rXM5cRljy7fTxHc45/view?usp=sharing)**
        or **[5.2.1(32bit OS)](https://drive.google.com/file/d/1cMEwkuLqWGxQiT7p97at_K7hI9Z8F40d/view?usp=sharing)**

   - This release is based on new [wayland architecture](https://www.raspberrypi.com/news/bookworm-the-new-version-of-raspberry-pi-os/), 
        please see [known issues](https://help.pisignage.com/hc/en-us/articles/26593998005785) and if it is 
     show-stopper, use legacy release (also called as 4.9.0 release in some places) which is available at [5.1.0_legacy based on Dec 2023 Raspberry Legacy(bulls eye) OS](https://pisignage.s3.amazonaws.com/pisignage-images/pisignage_5.1.0-legacy.img.zip) 

*For Raspberry Pi model 3 and model Pi Zero 2 W*   

   - Use [3.2.9 based on Raspberry Buster OS ](https://pisignage.s3.amazonaws.com/pisignage-images/pisignage_3.2.9.img.zip) or [3.2.9 Gdrive link](https://drive.google.com/file/d/1LlM0DHkmS2YLwTkemZocCvcdxi0c8PTZ/view?usp=sharing)     
   - 5.2.1 will also work, but may have performance issues.

*For Pi Zero/Pi 1/Compute-Model-1/Pi 2*
    
   - Use [3.2.9-armv6 image](https://pisignage.s3.amazonaws.com/pisignage-images/pisignage_3.2.9-armv6.img.zip)
   
*For [Radxa Rock 4C+ ONLY](https://za.rs-online.com/web/p/rock-sbc-boards/2493158)* 
     
   - Use [4.9.0 image](https://pisignage.s3.amazonaws.com/pisignage-images/pisignage_4.9.0_rock4Cplus.img.gz)  


##### 2. Use an application such as [Raspberry Pi Imager](https://www.raspberrypi.com/software/)(use custom option for OS 
   and **_do not use additional customizations like ssh, wifi, autologin etc. as it will be configured by piSignage_**) 
   or [balena Etcher](https://www.balena.io/etcher/) to program the downloaded image to a SD card. 
   - PS: *Simple copy-paste of the file into the SD card will not work.*

##### 3. Insert the programmed SD card into the Raspberry Pi and power ON.

##### 4. Register your player with player id at [pisignage.com](https://pisignage.com/players) to manage from the cloud.

##### 5. Get in touch with us at support@pisignage.com for any assistance. 

<a id="advanced"></a>
### Method 2: Mainual install on top of Raspbian OS/Debian/Ubuntu variants

You could install player2 on top of standard Raspberry OS or Debian/Ubuntu OS for other platforms yourselves. 
  - [Please click this link for instructions on how to install](https://pisignage.com/releases/Player2_installation_procedure.html). 

### More Resources

1. To manage players using your own local Server use [piSignage open-source server code](https://github.com/colloqi/pisignage-server)
2. To experience piSignage player in the browser, you could load [webapp](https://pisignage.com/player2/) in browser

### Android app
We encourage you to download the Android app for piSignage from Google Play Store. [Download link](https://play.google.com/store/apps/details?id=com.pisignage.player2&hl=en&gl=US)

But you need APK for some reason you can download from here [4.9.3.8](https://drive.google.com/file/d/15YyQGmQXBN0J380WmQktojy8Vzff-fv0/view?usp=sharing)

## Installing piSignage video 
 
[![Installing piSignage Video](http://img.youtube.com/vi/0o5cSq3Lwcg/0.jpg)](https://www.youtube.com/channel/UCyeItfgq72JUtzkQgcxYkKg)

### Few Points to remember

- Default Username & Password: use pi & pi 
- Player webUI: http://player-ip:8000
- Ctrl+N or F6: for network/server config from USB keyboard
- Ctrl+Alt+T or F2 for terminal

### SUPPORT

Refer [piSignage support page](https://help.pisignage.com/hc/en-us)

### Issues?

Raise your [issues here](https://www.pisignage.com/homepage/contact.html) or write to us at support@pisignage.com. 





