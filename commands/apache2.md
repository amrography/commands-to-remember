# apache2 <!-- omit in toc -->

- [403 issue](#403-issue)
- [Install and switch php version](#install-and-switch-php-version)

## 403 issue

`sudo nano \etc\apache2\sites-avalible\000-default.conf`

```xml
<VirtualHost *:80>
    ServerAdmin webmaster@localhost

    DocumentRoot /var/www
    <Directory />
        Options FollowSymLinks
        AllowOverride None
    </Directory>
    <Directory /var/www/>
        Options Indexes FollowSymLinks MultiViews
        AllowOverride None
        Order allow,deny
        allow from all
    </Directory>

    ScriptAlias /cgi-bin/ /usr/lib/cgi-bin/
    <Directory "/usr/lib/cgi-bin">
        AllowOverride None
        Options +ExecCGI -MultiViews +SymLinksIfOwnerMatch
        Order allow,deny
        Allow from all
    </Directory>

    ErrorLog ${APACHE_LOG_DIR}/error.log

    # Possible values include: debug, info, notice, warn, error, crit,
    # alert, emerg.
    LogLevel warn

    CustomLog ${APACHE_LOG_DIR}/access.log combined
</VirtualHost>
```

Then make sure you set the right permission like this:

```shell
sudo adduser <username> www-data
sudo chown -R www-data:www-data /var/www
sudo chmod -R g+rw /var/www
```

## Install and switch php version

1. Install php5

   `sudo apt-get install apache2 php5 libapache2-mod-php5`

2. Check if module is loaded

    `a2query -m php5`

3. Enable if not enabled

   `sudo a2enmod php5`

4. Restart apache2

    `sudo service restart apache2`
