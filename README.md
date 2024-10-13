# azureubuntu
How to create a good ubuntu rdp

sudo apt update && sudo apt upgrade -y

sudo apt install ubuntu-desktop -y


sudo apt install tigervnc-standalone-server tigervnc-xorg-extension -y

nano ~/.vnc/xstartup

 #!/bin/bash
unset SESSION_MANAGER
unset DBUS_SESSION_BUS_ADDRESS

# Log output for debugging
exec > /tmp/vncstartup.log 2>&1

# Start GNOME session
exec /usr/bin/gnome-session --session=ubuntu

# worked for ubuntu vm

vncserver -geometry 1920x1080 :2
