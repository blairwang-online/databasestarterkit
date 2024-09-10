# databasestarterkit
Starter kit for MariaDB backend and graphical frontends for Mac and Windows

Please note: these instructions should be used for development and learning purposes only. Additional security hardening would be required for using MariaDB in production environments!

## Mac instructions

1. Setup the **Homebrew** package manager using the instructions at https://brew.sh/

2. Since you already have **Terminal** open from the previous step, use it to get Homebrew to install MariaDB:

	```zsh
	brew install mariadb
	```

3. Once MariaDB is then installed, get it to run in the background:

	```zsh
	brew services start mariadb
	```

4. Now you will need to configure the security:

	```zsh
	sudo mariadb-secure-installation
	```
	
	Advice for how to fill out the form:
	- For _"current password for root"_, just hit <kbd>ENTER</kbd> ("return" key on Apple-branded keyboards) because there should be no password set yet.
	- For _"Switch to unix_socket authentication [Y/n]"_", just say "n" for "no", then hit <kbd>ENTER</kbd>.
	- For _"Change the root password? [Y/n]"_, say "y" for "yes",  then hit <kbd>ENTER</kbd>.. It will prompt you for a new password. Please enter something you will remember! Please note that you will not get any "&bull;&bull;&bull;&bull;&bull;&bull;" indicators that your password is being entered, but just type it in anyway, then hit <kbd>ENTER</kbd> when you're done. Please also note that you will be asked to enter your password again to confirm.
	- For _"Remove anonymous users? [Y/n]"_, say "y" for "yes", then hit <kbd>ENTER</kbd>.
	- For _"Disallow root login remotely? [Y/n]"_, say "y" for "yes", then hit <kbd>ENTER</kbd>.
	- For _"Remove test database and access to it? [Y/n]"_, say "y" for "yes", then hit <kbd>ENTER</kbd>.
	- For _"Reload privilege tables now? [Y/n]"_, say "y" for "yes", then hit <kbd>ENTER</kbd>.
	
5. Now that MariaDB is all set up to run in the background, you can install the frontend software, _Sequel Ace:_

	```zsh
	brew install --cask sequel-ace
	```

## Windows instructions

1. Download and install **XAMPP** from https://www.apachefriends.org/

2. Download and install **HeidiSQL** from https://www.heidisql.com/

## Acknowledgements

- Mac instructions adapted from https://getgrav.org/blog/macos-ventura-apache-mysql-vhost-apc

