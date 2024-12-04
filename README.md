# linux-android-setup

#install termux apk 
```
https://github.com/termux/termux-app
```
#termux-x11 apk
```
https://github.com/termux/termux-x11
```

#open termux app and run command
```
pkg update -y
pkg install wget -y
pkg install x11-repo -y
pkg install termux-x11-nightly -y
pkg install pulseaudio -y
pkg install xfce4 -y
pkg install tur-repo -y
pkg install chromium -y
pkg install termux-x11 -y
```

#switch to x11 repo
```
termux-change-repo
```

#download script
```
cd ~
wget https://raw.githubusercontent.com/LinuxDroidMaster/Termux-Desktops/main/scripts/termux_native/startxfce4_termux.sh
```

#run script
```
bash startxfce4_termux.sh
```

#=====================================
#some workaround to fix crash (if any)

#if your phone is samsung, run this command line first
```
export ADB_SERVER_SOCKET=localfilesystem:$(pwd)/adb_socket
adb start-server
adb devices
```

run this command
```
adb shell "/system/bin/device_config set_sync_disabled_for_tests persistent"
adb shell "/system/bin/device_config put activity_manager max_phantom_processes 2147483647"
adb shell settings put global settings_enable_monitor_phantom_procs false
```
