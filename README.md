# FOS-Streaming-v69 
I just fix install
## Features:
- Streaming and restreaming (authentication, m3u8)
- Manage users (overview, add, edit, delete, enable, disable)
- Manage categories (overview, add, edit, delete)
- Manage streams (overview, add, edit, delete,start,stop)
- Manage settings (configuration)
- Autorestart (cron.php need to set manual)
- Transcode -y
- Last IP connected
- h264_mp4toannexb
- play stream
- Playlist import
- Multiple streams on one channel
- Limit streams on users
- IP Block
- User Agent block
- predefined transcode profiles


## Installation
1. **`SUPPORTED DISTRO : Debian 9, 64 BIT`**
2. **`su`**
3. **`cd`**
4. **`apt-get install curl -y`**
5. **`curl -s https://raw.githubusercontent.com/Hidri2411/hidri/main/fos-stream-panel-v69 | bash`**
6. **`Visit : http://your-ip:7777/ login with User : admin Password : admin`**
7. **`Change "Web ip: *" with your public IPv4 server ip at http://your-ip:7777/settings.php`**
8. crontab -e `*/2 * * * * /etc/alternatives/php /home/fos-streaming/fos/www/cron.php`
9. **`Mysql Password : cat /root/MYSQL_ROOT_PASSWORD`**


### Change port of panel
1. change port in webinterface -> Settings -> web Port
2. change port in /home/fos-streaming/fos/nginx/conf/nginx.conf -> listen 8000;
3. `killall nginx; killall nginx_fos`
4. `/home/fos-streaming/fos/nginx/sbin/nginx`

## How can I use it?
- Default login: admin / admin
  - Add user
  - Add stream and use defined transcode profile 1 called **Default 1**
- You can use it also in proxy mode, but that depends on how you want to use it.
- The most stable way is using transcode profile: **Default 1** without proxy mode ticket

## Sources
1. FOS-Streaming-v1
2. ffmpeg
3. nginx, nginx-rtmp-module, nginx-geoip2-module
4. https://github.com/theraw -- ƬHE ЯAW ☣
