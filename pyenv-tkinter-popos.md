# Enable tkinter support in pyenv.

+ OS: Pop OS 22.04 
+ pyenv version: `3.10.4` 
+ `sudo apt install tk-dev`  

```
apt-file list tk-dev
tk-dev: /usr/include/tk
tk-dev: /usr/lib/tkConfig.sh
tk-dev: /usr/lib/x86_64-linux-gnu/libtk.a
tk-dev: /usr/lib/x86_64-linux-gnu/libtk.so
tk-dev: /usr/lib/x86_64-linux-gnu/libtkstub.a
tk-dev: /usr/lib/x86_64-linux-gnu/pkgconfig/tk.pc
tk-dev: /usr/lib/x86_64-linux-gnu/tkConfig.sh
tk-dev: /usr/share/doc/tk-dev/README.Debian
tk-dev: /usr/share/doc/tk-dev/changelog.gz
tk-dev: /usr/share/doc/tk-dev/copyright
```

+ Setup python configure option 
`export PYTHON_CONFIGURE_OPTS="--with-tcltk-includes='-I/usr/include/tk' --with-tcltk-libs='-L/usr/lib/x86_64-linux-gnu/'"`

+ `pyenv install 3.11.3`

```
Installing Python-3.11.3...
python-build: use tcl-tk from $PYTHON_CONFIGURE_OPTS
Installed Python-3.11.3 to /home/oxygen/.pyenv/versions/3.11.3
```

+ check if it works 

```
Python 3.11.3 (main, Apr 19 2023, 08:51:13) [GCC 11.3.0] on linux
Type "help", "copyright", "credits" or "license" for more information.
>>> import tkinter as tk
>>>
```

+ DONE
