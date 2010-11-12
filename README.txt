dkLab vzset: set barier/limit for OpenVZ UBC option interactively.
(C) dkLab, http://en.dklab.ru/lib/dklab_vzset/

Vzset is a very tiny utility which allows you to view current UBC
option value of OpenVZ container and type+apply a new value to
this option. This is useful when you receive a "limit exceeded"
notification by mail (e.g. over Yabeda or vzwatchd) and want to
increase an option fast.


INSTALLATION
------------

cd /usr/sbin
wget http://github.com/DmitryKoterov/dklab_vzset/raw/master/vzset
chmod +x vzmem


SYNOPSIS
--------

Bellow is a log of typical vzset session (an administrator typed
a new value "4703360" and pressed "y" to confirm).

# vzset 10002 tcpsndbuf
Current tcpsndbuf = 1720320:2703360
Enter new value (format is BARRIER:LIMIT or just LIMIT): 4703360
Accepted new value 4703360:4703360. Apply (y/n)? y
vzctl set 10002 --tcpsndbuf 4703360:4703360 --save
UB limits were set successfully
Saved parameters for CT 10002

