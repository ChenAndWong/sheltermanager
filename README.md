# sheltermanager

## server set up

This is a Debian server on Digital Ocean. It is under a "Team", called "Chen and Wong Consulting". Operational emails are currently going to Ruth's personal email address.

The server is running in Toronto.

### shelter manager

We are installing Shelter Manager ASM 3 series: https://sheltermanager.com/site/en_oss_asm3.html

sheltermanager set up instructions: https://github.com/sheltermanager/asm3

i have NOT set up the crons.

1. install shelter manager debian package
2. install sqlite3 - db is /var/www/asm.db
3. `sudo ln -s /var/www/sheltermanager/asm3.service /etc/systemd/system/asm3.service`
4. `sudo systemctl enable asm3.service`
5. 
```
sudo ln -s /var/www/sheltermanager/shelterdemo.initial_nginx /etc/nginx/sites-available/shelterdemo
sudo ln -s /var/www/sheltermanager/shelterdemo.initial_nginx /etc/nginx/sites-enabled/shelterdemo
sudo systemctl reload nginx
```
6. Make sure DNS for shelterdemo.chenandwong.consulting is set up in digital ocean if you haven't already.
6. `sudo certbot certonly --webroot -w /var/www/sheltermanager -d shelterdemo.chenandwong.consulting -d www.shelterdemo.chenandwong.consulting`
7. ```
sudo ln -sf /var/www/sheltermanager/shelterdemo.nginx /etc/nginx/sites-available/shelterdemo
sudo ln -sf /var/www/sheltermanager/shelterdemo.nginx /etc/nginx/sites-enabled/shelterdemo
```
### sqlite3 setup

apt-get install sqlite3
sqlite3 asm
ask Ruth for the db password

