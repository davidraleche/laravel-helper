##  Quick Setup SQL LITE
```
- touch Database/database.sqlite
- then update .env
```
##  create Key AES KEY
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
## Logs
### laravel Log Viewer

Install via composer
```
composer require rap2hpoutre/laravel-log-viewer
```
Add Service Provider to config/app.php in providers section
```
Rap2hpoutre\LaravelLogViewer\LaravelLogViewerServiceProvider::class,
```

Add a route in your web routes file:
```
Route::get('logs', '\Rap2hpoutre\LaravelLogViewer\LogViewerController@index');
```
Go to http://myapp/logs or some other route
Optionally publish log.blade.php into /resources/views/vendor/laravel-log-viewer/ for view customization:
```
php artisan vendor:publish \
  --provider="Rap2hpoutre\LaravelLogViewer\LaravelLogViewerServiceProvider" \
  --tag=views
  ```
