Mecord Python Tool
===============================================
The Mecord Python Tool is a official tool for mecodr, you can use it to **Register** device to mecord server, other person can use **Mecord Application** assign tasks to you for implementation

Installation
------------

The Mecord requires [Python](http://www.python.org/download) 3.10.6 or later.

##### Installing
    pip install mecord-cli

##### Uninstalling
    pip uninstall mecord-cli

Use
------------
##### 1. RegisterDevice To Mecord Server
    $ mecord deviceid
use mecord mobile application scan qrcode to register your device to mecord server

##### 2. Running
    $ mecord service start
start a process to wait for the server to issue tasks. **Please do not close it**

Module Developer
------------
    $ mecord widget init

in empty folder, use above command craete a mecord module, structure is like 
    
    [widget folder]
        |-- h5
            |-- config.json     //*required, do not change*
            |-- icon.png
            |-- index.html      //*required* index web page
            |-- MekongJS.js      //*required, do not change*
        |-- script
            |-- main.py         //*required, do not change* 
            |-- run.py

if other person share widget code to you , you can add widget path in your computer to mecord environment

    $ mecord widget add [path_with_widget_code]

you can modify script and h5 file yourself, then publish to mecord sever 
    
    $ mecord widget publish

#####other command
set/get multi process task number

    $ mecord set_multitask_num / get_multitask_num 1

add this device joined to other group using token, or show current group token , you can share it to other person

    $ mecord add_token /  show_token [token_string]

unregister this device from mecord server

    $ mecord unbind