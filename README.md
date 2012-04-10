# nginx-init-debian

Upstart & System V init scripts for debian-based distributions such as Ubuntu, Mint, Mepis, etc.


### Upstart

```sh
git clone  git@github.com:hulihanapplications/nginx-init-debian.git
cd nginx-init-debian
sudo cp etc/init/nginx.conf /etc/init
# Start Nginx
sudo start nginx 
```

* By default, the script thinks nginx is in `/opt/nginx`. If your nginx configuration is different, edit `/etc/init/nginx.conf` and change it to the correct location.

### System V

```sh
git clone  git@github.com:hulihanapplications/nginx-init-debian.git
cd nginx-init-debian
sudo cp etc/init.d/nginx /etc/init.d
sudo chown root:root /etc/init.d/nginx
sudo chmod 755 /etc/init.d/nginx
# Start nginx 
sudo /etc/init.d/nginx start
```

* By default, the script thinks nginx is in `/opt/nginx`. If your nginx configuration is different, edit `/etc/init.d/nginx` and change it to the correct location:
  
```sh
DAEMON=/opt/nginx/sbin/nginx
NGINX_CONF_FILE="/opt/nginx/conf/nginx.conf"
```

### License - MIT X11

Permission is hereby granted, free of charge, to any person obtaining a copy of this
software and associated documentation files (the "Software"), to deal in the Software
without restriction, including without limitation the rights to use, copy, modify, merge,
publish, distribute, sublicense, and/or sell copies of the Software, and to permit 
persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or 
substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING 
BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND 
NONINFRINGEMENT. IN NO EVENT SHALL THE X CONSORTIUM BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER 
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN 
CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.

### Copyright

Dave Hulihan &copy; 2012 - [Hulihan Applications](http://www.hulihanapplications.com) 

### Credits

* [Big Rock Software's nginx upstart script](http://blog.bigrocksoftware.com/2011/01/07/rvm-nginx-passenger-rails-3/)
* [Jason Giedymin's nginx-init-ubuntu script](http://code.google.com/p/nginx-init-ubuntu/) 
