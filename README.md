# raspi-love
Raspi display to display random messages. 
[Pi 4 Touch Screen with Case, 3.5 inch Touchscreen]( https://www.amazon.com/gp/product/B07WQW6H9S/ref=ppx_yo_dt_b_search_asin_title?ie=UTF8&psc=1 )
[Pi4 Starter Kit](https://www.amazon.com/gp/product/B07VXBMWQK/ref=ppx_yo_dt_b_search_asin_title?ie=UTF8&psc=1) or any suitable Raspberry Pi

# Install Raspbian
1. Download Raspbian latest desktop https://downloads.raspberrypi.org/raspbian_latest
1. Burn to card with Raspberry Pi Imager: https://downloads.raspberrypi.org/imager/imager.exe 
      This is new but seems to work though slower than win32DiskImager. Also, obviates the need to pre-download the image. 
1. Once burned, insert the card into your RPI, boot, configure networking, etc as you like.  
1. Connect the raspberry pi to a keyboard, mouse and monitor and configure it to work with your network. 
1. sudo apt install git
1. git clone https://github.com/goodtft/LCD-show.git 
1. chmod -R 755 ./LCD-show/
1. cd LCD-show/
1. sudo ./MHS35-show  (note: once these drivers are loaded hdmi will no longer work. to turn it back on, run sudo ./LCD-hdmi in the same directory)
1. sudo ./rotate.sh 180 (flips the screen orientation)
1. power down the raspberry pi and install the touchscreen  

# Set up Kiosk Mode
1. ssh into your box
1. sudo raspi-config 
  1. Boot Optons
    1. Desktop CLI
      1. Console Autologin
  1. Advanced Options
    1. Overscan
      1. No/OK
  1. Finish, Ok, Reboot.
1. ssh in
1. sudo vi /lib/systemd/system/kiosk.service
1. 
