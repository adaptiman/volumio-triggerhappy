# volumio-triggerhappy
Here’s an updated config file for triggerhappy with extended functionality that works with the hifiberry USB remote and the current build of Volumio (2.907). Here are the contents of /etc/triggerhappy/triggers.d/audio.conf

```
#VOLUMIO TRIGGERHAPPY CONFIGURATION FILE

#MUTE TOGGLE
KEY_HOME 1 /usr/local/bin/volumio volume toggle

#VOLUME UP
KEY_VOLUMEUP 1 /usr/local/bin/volumio volume plus

#VOLUME DOWN
KEY_VOLUMEDOWN 1 /usr/local/bin/volumio volume minus

#PLAY PAUSE TOGGLE
KEY_ENTER 1 /usr/local/bin/volumio toggle

#FAST FORWARD 10 SECONDS
KEY_UP 1 /usr/local/bin/volumio seek plus

#REWIND 10 SECONDS
KEY_DOWN 1 /usr/local/bin/volumio seek minus

#NEXT SONG
KEY_RIGHT 1 /usr/local/bin/volumio next

#PREVIOUS SONG
KEY_LEFT 1 /usr/local/bin/volumio previous

#TOGGLE RANDOM
KEY_COMPOSE 1 /usr/local/bin/volumio random

#TOGGLE REPEAT
KEY_ESC 1 /usr/local/bin/volumio repeat

#CLEAR CURRENT QUEUE
KEY_POWER 1 /usr/local/bin/volumio clear
```
After editing, you must restart the service with

```
sudo /etc/init.d/triggerhappy reload
```
Functions of each key are listed in the comments above the command.

IMPORTANT NOTE: This remote has a mouse control button in the upper right of the control. This button toggles mouse mode and totally messes up the mapping, making the remote almost useless. Don’t push it, don’t map it, and the keys above will work just fine.

After editing, you must restart the service with

sudo /etc/init.d/triggerhappy reload
