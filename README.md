# First
### The IP address: 157.230.144.82
### SSH port: 2200
# Second
[Here is a link to the website](http://157.230.144.82.xip.io/)
# Third
The first thing i did when I ran the server is update the package by using `sudo apt-get update` and upgrade using `sudo apt-get upgrade`

I installed some softwares:
#### apache:
the apache server downloaded using `sudo apt-get install apache2`
#### pip:
the pip (which is for python) downloaded using `sudo apt-get install python-pip`

then I installed some technologies from the pip such as:
#### sqlalchemy
downloaded using `pip install sqlalchemy`
#### flask
downloaded using `pip install flask`
#### requests
downloaded using `pip install requests`
#### oauth2client
downloaded using `pip install oauth2client`

And there are some configurations that applied:
#### WSGI
allow apache to hand-off certain requests to an application handler. So first download it using `sudo apt-get install libapache2-mod-wsgi` and then edit the `/etc/apache2/sites-enabled/000-default.conf` file by adding this line `WSGIScriptAlias / /var/www/myapp.wsgi` before the end of block `</VirtualHost>`. Then write this command `sudo nano /etc/apache2/apache2.conf` it will show a blank file, so write this line to solve the "ServerName" problem `ServerName localhost`. Then restart the server using `sudo service apache2 restart`.
#### Firewall
This server will allows three ports: 2200 (SSH), 80 (HTTP), 123 (NTP).
To allow these ports we will write these commands:
`sudo ufw allow 2200`
`sudo ufw allow 80`
`sudo ufw allow 123`
then enable the firewall using `sudo ufw enable`

# Fourth
### Here is some resources that help me:
- Slack channels
- StackOverflow posts
- askubuntu website
- Search in google
- Github repos
