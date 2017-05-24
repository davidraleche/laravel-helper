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
## Unix Alias
```
alias p=phpunit
alias pf='phpunit --filter'```

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
  
  ## Sublime install  control package (https://packagecontrol.io/installation#st2)
  >View > Show Console
  
  for sublime 2
  ```
  import urllib2,os,hashlib; h = 'df21e130d211cfc94d9b0905775a7c0f' + '1e3d39e33b79698005270310898eea76'; pf = 'Package Control.sublime-package'; ipp = sublime.installed_packages_path(); os.makedirs( ipp ) if not os.path.exists(ipp) else None; urllib2.install_opener( urllib2.build_opener( urllib2.ProxyHandler()) ); by = urllib2.urlopen( 'http://packagecontrol.io/' + pf.replace(' ', '%20')).read(); dh = hashlib.sha256(by).hexdigest(); open( os.path.join( ipp, pf), 'wb' ).write(by) if dh == h else None; print('Error validating download (got %s instead of %s), please try manual install' % (dh, h) if dh != h else 'Please restart Sublime Text to finish installation')

  ```
