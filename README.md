# ALVRUSBGuide
An alternative guide for setting up ALVR over USB using a link cable and a supported headset.

# How to use wired PCVR on Quest without Oculus software

## Things you need:
### ALVR Launcher - This will install the most updated version of the ALVR Dashboard, which is necessary for hooking up your quest to your pc without using Oculus software. Link to download can be found here: <https://github.com/alvr-org/ALVR>. *Do not clone the repo, look for the link inside of it that says "Windows Launcher".*
### ADB Forwarder - This will connect your quest to your PC via adb and automatically reconnect if your cable disconnects temporarily - this is neccessary to transmit TCP signals over USB, which is how ALVR wired connection works. Link to download can be found here: <https://github.com/alvr-org/ADBForwarder>
### VB-Audio - This will pass speaker and microphone audio between your computer and headset, allowing you to hear and speak through your headset. ALVR will automatically prompt you to install VB-Audio.
### USB2.0 or 3.0 USB-C to USB-C/USB-A Cable - This will be the cable that actually transmits all the data from your computer to the headset. My recommendation can be bought here: <https://www.kiwidesign.com/products/link-cable-compatible-with-quest-3>
### SteamVR - This is the VR runtime that you will be using. Link to download can be found here: <https://store.steampowered.com/app/250820/SteamVR/>
### Developer mode on your Quest 2. Detailed instructions on developer mode will be found below.

## Developer mode setup:
1. Log into your meta account in the Meta Developer website. Link can be found here: https://developer.oculus.com/manage/organizations/create/
2. In the developer dashboard, verify your account with 2FA or the card you use to purchase games.
3. Go back to the link provided above, and create an organisation if you haven't already. This can be named anything, as long as it is unique. Accept TOS and NDA and submit.
4. Turn on your headset and place it somewhere nearby, and open the Meta Horizon app on your phone.
5. Click the icon that shows your headset in the app, and go into headset settings.
6. Go to developer mode and enable it.

## Installation steps for ALVR:
1. Extract the zip file obtained from the ALVR github repo, and open the alvr-launcher-windows folder. 
2. Run the exe named ALVR Launcher. It will prompt you to download a new build of ALVR, go through the dialogue and install it.
3. Through the launcher, run ALVR Dashboard.
4. Go through the first time setup, including installing the ALVR drivers, ALVR Firewall and VB-Audio drivers.
5. Go to your quest. Inside the headset, look for ALVR on the quest store. Download the free app for it.

## Configuration steps for ALVR:
1. Inside of the ALVR dashboard on PC, open the settings and go to the Connection tab.
2. Switch the stream protocol from UCP to TCP.
3. Launch SteamVR using the button inside of ALVR, and launch the ALVR client inside of your headset. **Make sure your headset is connected to the same network as your pc.**
4. If your computer doesnt auto-detect your headset, add a new device manually in the devices, and make the IP 127.0.0.1, and make the hostname whatever is found inside of the ALVR app inside of your headset. Mark it as a trusted device. 
5. It is now safe to close SteamVR.

## Installation steps for ADBForwarder:
1. Extract the zip file obtained from the ADBForwarder github repo, and open the folder it creates
2. Run the exe named ADBForwarder.
3. Let ADBForwarder install ADB if it isnt already on your pc.
4. Accept the firewall rules.

## Configuration steps for ADBForwarder:
1. Once ADBForwarder is running, connect your headset to your computer with your cable. 
2. Inside of your headset, click "Always trust this computer" or "Yes" on the prompt asking to trust this computer for ADB.
3. ADBForwarder will now tell you to unplug and replug your headset. Do so as instructed, and then ADBForwarder should automatically connect your quest to ADB. You may need to restart ADBForwarder.
