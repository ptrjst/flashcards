# Homebrew

### How do you get all the new versions formulas from the Homebrew server?

	brew update

This downloads all of the new formulas from Homebrew. However, it does not install anything. You must do this manually by saying:

	brew upgrade mysql

### How do you list all the outdated packages?

	brew outdated

### How do you get all of the versions available for a formula?

	$ brew versions mysql
	5.6.12   git checkout ba37612 /usr/local/Library/Formula/mysql.rb
	5.6.10   git checkout 48f7e86 /usr/local/Library/Formula/mysql.rb
	5.5.29   git checkout 336c976 /usr/local/Library/Formula/mysql.rb
	5.5.28   git checkout 5825f62 /usr/local/Library/Formula/mysql.rb
	5.5.27   git checkout 93aecfa /usr/local/Library/Formula/mysql.rb
	5.5.25a  git checkout faaa6c1 /usr/local/Library/Formula/mysql.rb
	5.5.24   git checkout a977fbd /usr/local/Library/Formula/mysql.rb
	5.5.20   git checkout f4009ef /usr/local/Library/Formula/mysql.rb
	5.5.19   git checkout c2b8e87 /usr/local/Library/Formula/mysql.rb
	5.5.15   git checkout 513c0f8 /usr/local/Library/Formula/mysql.rb
	5.5.14   git checkout a840c4a /usr/local/Library/Formula/mysql.rb
	5.5.12   git checkout 35b60ca /usr/local/Library/Formula/mysql.rb
	5.5.10   git checkout 1f2b24e /usr/local/Library/Formula/mysql.rb
	5.1.56   git checkout feae63a /usr/local/Library/Formula/mysql.rb
	5.1.55   git checkout 0476235 /usr/local/Library/Formula/mysql.rb
	5.1.54   git checkout 7077f84 /usr/local/Library/Formula/mysql.rb
	5.1.53   git checkout fbee3a0 /usr/local/Library/Formula/mysql.rb
	5.1.52   git checkout 7871a99 /usr/local/Library/Formula/mysql.rb
	5.1.51   git checkout 0fc5ce3 /usr/local/Library/Formula/mysql.rb
	5.1.49   git checkout 2e7d624 /usr/local/Library/Formula/mysql.rb
	5.1.48   git checkout 75def21 /usr/local/Library/Formula/mysql.rb
	5.1.47   git checkout 9d73887 /usr/local/Library/Formula/mysql.rb
	5.1.46   git checkout ee9ecec /usr/local/Library/Formula/mysql.rb
	5.1.45   git checkout 1ca6b6b /usr/local/Library/Formula/mysql.rb
	5.1.44   git checkout 052d1f2 /usr/local/Library/Formula/mysql.rb
	5.1.43   git checkout c4decd7 /usr/local/Library/Formula/mysql.rb


### What does it mean for something to be "pinned"?

The something is a package. Pinning a package locks its version, preventing it from being upgraded.

### How do you get a list of the pinned packages?

	brew list --pinned
	
