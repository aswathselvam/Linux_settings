.mp4 to .gif
```
ffmpeg -i 3d.webm -r 10 -vf scale=-1:-1 -ss 00:00:02 -to 00:00:30 3d.gif
```

## Linux packages:

All packages:
```
sudo dpkg --get-selections > ./app-backup-list.txt
```

ROS packages list:
```
sudo dpkg --get-selections | grep ros > ./ros-backup-list.txt 
```

Restore:
```
sudo dpkg --get-selections < app-backup-list.txt
sudo apt-get -y update
sudo apt-get dselect-upgrade
```