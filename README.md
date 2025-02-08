Personal repo for running Klipper suite for 3D printers on android phone. These are my configuration files, no passwords in them, so useless for you.

If you need help how to install klipper on android follow this guide: https://github.com/d4rk50ul1/klipper-on-android

#Fix Klipper service

sudo wget -O /etc/default/klipper https://raw.githubusercontent.com/ant0nant0n0v/klipperfixpublic/main/default/klipper

sudo wget -O /etc/init.d/klipper https://raw.githubusercontent.com/ant0nant0n0v/klipperfixpublic/main/init.d/klipper

#Fix Moonraker service

sudo wget -O /etc/default/moonraker https://raw.githubusercontent.com/ant0nant0n0v/klipperfixpublic/main/default/moonraker

sudo wget -O /etc/init.d/moonraker https://raw.githubusercontent.com/ant0nant0n0v/klipperfixpublic/main/init.d/moonraker

sudo wget -O /home/thw/printer_data/config/moonraker.conf https://raw.githubusercontent.com/ant0nant0n0v/klipperfixpublic/main/printer_data/config/moonraker.conf

#Fix Nginx service

sudo wget -O /etc/default/nginx https://raw.githubusercontent.com/ant0nant0n0v/klipperfixpublic/main/default/nginx

sudo wget -O /etc/init.d/nginx https://raw.githubusercontent.com/ant0nant0n0v/klipperfixpublic/main/init.d/nginx

sudo wget -O /etc/nginx/nginx.conf https://raw.githubusercontent.com/ant0nant0n0v/klipperfixpublic/main/nginx/nginx.conf

#Fix Anycubic vyper klipper configuration

sudo wget -O /home/thw/printer_data/config/printer.cfg https://raw.githubusercontent.com/ant0nant0n0v/klipperfixpublic/main/printer_data/config/printer.cfg

#Fix Xterm

sudo wget -O /usr/local/bin/xterm https://raw.githubusercontent.com/d4rk50ul1/klipper-on-android/main/scripts/usr_local_bin_xterm

#Files permissions fixes

sudo chmod +x /etc/init.d/klipper

sudo chmod +x /etc/init.d/moonraker

sudo chmod +x /usr/local/bin/xterm

sudo update-rc.d klipper defaults

sudo update-rc.d moonraker defaults

sudo chmod 777 /dev/ttyACM0

sudo chmod 777 /dev/ttyUSB0

sudo chmod 777 /dev/pts/0

sudo chmod 777 /dev/pts/1

sudo chmod 777 /dev/pts/2

sudo chmod 777 /dev/pts/3

sudo chmod 777 /dev/pts/4

sudo chmod 777 /dev/pts/5

sudo chmod 777 /dev/pts/6
