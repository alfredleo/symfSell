
# Check apache logs
tail -f ~/lib/apache2/log/*.log

# Configure apache
sudo nano /etc/apache2/sites-enabled/001-cloud9.conf

# UPGRADE php to 7.2
```
sudo apt-get install python-software-properties -y
sudo add-apt-repository ppa:ondrej/php -y
sudo apt-get update -y
sudo apt-get install php7.2 php-pear php7.2-curl php7.2-dev php7.2-gd php7.2-mbstring php7.2-zip php7.2-mysql php7.2-xml php7.2-cli php7.2-intl php7.2-json php7.2-opcache php7.2-bcmath php7.2-soap -y
sudo apt-get install libapache2-mod-php7.2 -y
sudo a2dismod php5
or
sudo a2dismod php7.0
sudo a2enmod php7.2
sudo service apache2 restart
```

# Beautiful git log (usage git lg, git lg -p)
``` bash
git config --global alias.lg "log --color --graph --pretty=format:'%Cred%h%Creset -%C(yellow)%d%Creset %s %Cgreen(%cr) %C(bold blue)<%an>%Creset' --abbrev-commit"
```