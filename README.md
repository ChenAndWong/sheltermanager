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

### sqlite3 setup

apt-get install sqlite3
sqlite3 asm
ask Ruth for the db password

