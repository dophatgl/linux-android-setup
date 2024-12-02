# linux-android-setup

#install termux & termux-x11 apk
https://github.com/termux/termux-app
https://github.com/termux/termux-x11

#open termux app and run command
```
pkg update
pkg install wget
pkg install x11-repo
pkg install termux-x11-nightly
pkg install pulseaudio
pkg install xfce4
pkg install tur-repo
pkg install chromium
pkg install termux-x11
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
