# bluetooth-keepalive

This will help you if:
1. You use your macbook in clamshell mode with an external display most of the time.
2. When your macbook is docked, you use bluetooth accesories such as a keyboard or mouse.
3. When un-docking your macbook you turn bluetooth off to save battery life.
4. You always forget to turn it back on when docking so you have to open up the screen and turn bluetooth on manually.

Basically, we are creating a daemon to always check if your macbook's bluetooth is on and check if you are connected to your home/office network. If you are connected to home/office but bluetooth is off, it will turn it back on.

It is not perfect, but it does the job. Feel free to give some feedback to improve!

## How to use?
1. Edit the `bluetooth.scpt` script. 
    Open bluetooth.scpt using Script Editor and replace <YOUR_INTERFACE_HERE> with the network interface that you mostly use when connected to clamshell mode. I chose this because whenever I use clamshell mode I only use wired connection as opposed to wifi.
    Example : YOUR_INTERFACE_HERE -> en1

2. Place this script somewhere on your laptop and make note of the path.

3. Edit the `ethernet-bluetooth.plist` file
    Open the file using your favorite editor and replace PATH_TO_SCRIPT_HERE with the path to the script we edited in step 1.
    
4. Create the daemon
    Place the `ethernet-bluetooth.plist` file in `~/Library/LaunchAgents`

