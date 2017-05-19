## #1 Quick Setup SQL LITE
```
- touch Database/database.sqlite
- then update .env
```
## #2 create Key AES KEY
```
php artisan key:generate 
```
## Install Valet - local webserver
1 . In Terminal
```
/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
```
2 . in Terminal
```
brew install homebrew/php/php71
```
3. in terminal
```
composer global require laravel/valet
```

## Unix BASH path 
```
echo 'export PATH="$PATH:$HOME/.composer/vendor/bin"' >> ~/.bashrc
```
In order to check if it worked, logout and login again or execute
```
source ~/.bashrc
```
