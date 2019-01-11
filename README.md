# Virtual Machine (VM)
Installing a VM to work from during your training

## Installation of a vitual box vm
1. Download and install virtual box from https://www.virtualbox.org
2. Download and install the ubuntu image
    1. Got to https://www.osboxes.org/ubuntu/ and download the Virtual Box version of "Ubuntu 18.10 Cosmic Cuttlefish" (you will be forwarded to a sourceforge site and the download will start automaticaly)
    2. Unzip the image with 7zip and remember the location (if you down't have 7zip on your system, you can download it at https://www.7-zip.org/download.html)
    3. Open the virtual box application on you're system
    4. Click on "New" (this will setup a new virtual machine)
    5. Set the following parameters: Name="Ubuntu training", Type="Linux", Version="Ubuntu (64-bit)" (leave the Machine Folder on the default location) and click "Continue"
    ![alt text](https://raw.githubusercontent.com/Arend-Jan/vmsetup/master/images/Screenshot%202019-01-11%20at%2015.34.37.png)
    6. Give it some good amount of memory (suggest to give it at leasted 8GB of memory if you're system allows it, and click "Continue"
    ![alt text](https://raw.githubusercontent.com/Arend-Jan/vmsetup/master/images/Screenshot%202019-01-11%20at%2015.49.55.png)
    7. Select "Use an existing vitual hard disk file"
    ![alt text](https://raw.githubusercontent.com/Arend-Jan/vmsetup/master/images/Screenshot%202019-01-11%20at%2015.52.14.png)          
    8. Click the yellow folder icon    
    9. Click "Add" on the top
    10. Browse to the location where you extracted the image in step 2.2 and select the image and click "Open"
    ![alt text](https://raw.githubusercontent.com/Arend-Jan/vmsetup/master/images/Screenshot%202019-01-11%20at%2015.58.38.png)
    11. Select the "Ubuntu 18.10 Cosmic (64bit).vdi" and click Choose
    12. Click "Create" (the Ubuntu training machine should now apeare on the left side)
    ![alt text](https://raw.githubusercontent.com/Arend-Jan/vmsetup/master/images/Screenshot%202019-01-11%20at%2016.00.19.png)
3. Configure how the VM image will run
    1. Select the Ubuntu training machine (it should still be powered off)
    2. Click "Settings" -> "System" -> "Processor"
    3. Set the amount of Processor(s) to "2" and click "OK"
    ![alt text](https://raw.githubusercontent.com/Arend-Jan/vmsetup/master/images/Screenshot%202019-01-11%20at%2016.04.25.png)
4. Start your VM for the first time
    1. Select the "Ubuntu Training" machine
    2. Click the "Start" icon at the top, to start running the VM (this might take some time)
    3. Login to the osboxes.org account with the password "osboxes.org" (without the quotes)
    ![alt text](https://raw.githubusercontent.com/Arend-Jan/vmsetup/master/images/Screenshot%202019-01-11%20at%2016.10.49.png)
    4. You will be asked to setup an online account. We can ignore this by clicking "Skip" and a couple of times next
    5. It might be that there are software updates avaible. You can install them if you please (we recommend doing this)
    6. Click the icon with the 9 dots in the bottom left corner (We are going the change the display resolution, so we do have some more real estated to work with)
    ![alt text](https://raw.githubusercontent.com/Arend-Jan/vmsetup/master/images/Screenshot%202019-01-11%20at%2016.14.10.png)
    7. Type in "displays"
    8. Click on the line the the display icon the the text "Displays"
    ![alt text](https://raw.githubusercontent.com/Arend-Jan/vmsetup/master/images/Screenshot%202019-01-11%20at%2016.17.42.png)
    9. Select the "Resolution" with makes most sence to your system (we choice 1280 x 768, it might be better to choice a bigger resolution if you display is up to it) and click the green button on the top right corner
    10. The screen will change resolution, and if it fits your setup, you can keep the changes by clicking the apropriate butten
    ![alt text](https://raw.githubusercontent.com/Arend-Jan/vmsetup/master/images/Screenshot%202019-01-11%20at%2016.22.08.png)
    11. Close the Displays window by clicking the red X on the top right corner
## Update, upgrade and install software on Ubuntu
1. Click the icon with the 9 dots in the bottom left corner
2. Type "terminal" (an black icon with the text "Terminal" should appear)
3. Click the "Terminal" icon and type the following command (without the "$" and press enter after the command)
```Bash
$ sudo apt-get update
```
4. The system will askes for the sudo password. This password is the userpassword of osboxes.org account (so the password is "osboxes.org"). Type it in and press enter (the system updates the package lists for upgrades for packages that need upgrading)
5. After the update is done, enter the following command in the terminal (the system will upgrade all it's packages. this might take a while)
```Bash
$ sudo apt-get upgrade
```
### Install curl
1. If your not still in it, go to the terminal
2. Enter the following command 
```Bash
$ sudo apt-get install curl
```
3. The system will install curl. It might ask for a password (enter the password) and/or to agree to install some stuff (just enter "Y" and hit enter)
### Install mosquitto
1. If your not still in it, go to the terminal
2. Enter the following command 
```Bash
$ sudo apt-get install mosquitto mosquitto-clients
```
3. The system will install mosquitto. It might ask for a password (enter the password) and/or to agree to install some stuff (just enter "Y" and hit enter)
