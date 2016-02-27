**Disclaimer:** This is a fork of https://github.com/pablorusso/GoogleMusic.bundle `s [update_gmusicapi_fix_login](https://github.com/pablorusso/GoogleMusic.bundle/tree/update_gmusicapi_fix_login) 
branch modified to work with Plex Media Server in Linux (ubntu).

---

GoogleMusic.bundle linux build
==============================

A Plex plugin for Google Music. An All Access account is not required but many of the features will not work without one.

Installation Instructions
-------------------------

```
$ cd /var/lib/plexmediaserver/Library/Application Support/Plex Media Server/Plug-ins
$ git clone {this repo url}/GoogleMusic.bundle.git
$ sudo chown -R plex:plex GoogleMusic.bundle
$ sudo service plexmediaserver restart
````

Refresh web interface and look in channels.

Installing/Updating Crypto
--------------------------

If having issues opening the plugin. Steps from [here](https://github.com/jwdempsey/GoogleMusic.bundle/pull/13#issuecomment-140810883)

```
$ sudo apt-get install gcc python python-dev
$ wget https://pypi.python.org/packages/source/p/pycrypto/pycrypto-2.6.1.tar.gz
$ tar -xf pycrypto-2.6.1.tar.gz
$ cd pycrypto-2.6.1/
$ python setup.py build
$ sudo cp -R build/lib.linux-x86_64-2.7/Crypto /var/lib/plexmediaserver/Library/Application\ Support/Plex\ Media\ Server/Plug-ins/GoogleMusic.bundle/Contents/Libraries/Shared/
$ sudo chown -R plex:plex /var/lib/plexmediaserver/Library/Application\ Support/Plex\ Media\ Server/Plug-ins/
```

Thanks
------

Huge thanks to all the people who worked on this upstream [jwdempsy](https://github.com/jwdempsey/GoogleMusic.bundle), [supermaik](https://github.com/supermaik/GoogleMusic.bundle), [pablorusso](https://github.com/pablorusso/GoogleMusic.bundle)

