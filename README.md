# config_camlink_ubuntu

## installation
`sudo apt-get install -y v4l2loopback-dkms`

`sudo apt install v4l-utils`

`sudo apt  install ffmpeg`

## config
sudo modprobe v4l2loopback devices=1 exclusive_caps=1

ffmpeg -f v4l2 -input_format yuyv422 -framerate 60 -video_size 1920x1080 -i /dev/video0 -pix_fmt yuyv422 -codec copy -f v4l2 /dev/video2

## To change audio devices settings

pavucontrol
