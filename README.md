# A simple keylogger for Windows, Linux and Mac
[![MIT Licence](https://badges.frapsoft.com/os/mit/mit.png?v=103)](https://opensource.org/licenses/mit-license.php)

[Keylogger wiki](https://github.com/GiacomoLaw/Keylogger/wiki)

Welcome to the simple keylogger repo! A keylogger is a program that records your keystrokes, and this program saves them in a log file on your local computer. 

Check out below to learn how to install them. These keyloggers are simple and bare bones, however they work great! Feel free to fork and improve it if you want. Be sure to check out the [pull requests](https://github.com/GiacomoLaw/Keylogger/pulls) to see if your problem has been fixed, or to help out others.

Currently, there are three keylogger programs for the major operating systems; Windows, Mac and Linux. 

> Please note, currently there is no known way to track keylogs in secure areas on Macs, such as password input areas.

## Windows
Simply compile into an .exe, and then run. Visual Studio is good for this.

There are two files; klog_visible and klog_invisible. It is pretty simple, but I will expand:

- `klog_invisible` makes the window of the logger disappear, and it also starts up hidden from view. Note that it is still visible in the task manager.
- `klog_visible` is visible, and the window does not close when typing. Great for testing it out. 

Both of these save the keystrokes to a .txt file when closed.

## Mac
This is a little more complicated, as its Apple after all! Please note, it does not work for secure areas such as password inputs. I have not found a work around yet.

### Installation
Download the repo. It will install in `/usr/local/bin/keylogger`.

Install it:

`$ git clone https://github.com/GiacomoLaw/Keylogger && cd keylogger`

`$ make && make install`

It will log to `/var/log/keystroke.log`. This may require root access, but you can change that if you want. Set where you want it to log:

`$ keylogger ~/logfile.txt`

`Logging to: /var/log/keystroke.log`

Want to make it start on system startup?

`$ sudo make startup`

That will run it on startup.

### Uninstall
`$ sudo make uninstall`

Will uninstall the program, but not the logs.

---

Thanks to Casey Scarborough for the base program!

## Linux
### Installation
You'll need to install python-xlib if you don't have it.

`sudo apt-get install python-xlib`

Check that you have git installed, and then run this.

`git clone https://github.com/GiacomoLaw/Keylogger`

This will clone this entire repo. Find the linux folder, extract it, and open it. Rename the extracted folder to `linux-logger` Then run this:

`giacomo@vostro:~$ cd linux-logger/`

Set where you want the log to go **before** running this step.

`giacomo@vostro:~/linux-logger$ python keylogger.py`

`<class 'Xlib.protocol.request.QueryExtension'>`

`<class 'Xlib.protocol.request.QueryExtension'>`

`RECORD extension version 1.13`

The keylogger is now running! It will log your strokes to the file you specified. Stop it by hitting the grave key. Thats the one under escape on a standard keyboard.

You can make it run on startup:

`python /home/giacomo/py-keylogger/keylogger.py`

---
#### Uses

Some uses of a keylogger are:

- Business Administration: Monitor what employees are doing.
- School/Institutions: Track keystrokes and log banned words in a file.
- Personal Control and File Backup: Make sure no one is using your computer when you are away.
- Parental Control: Track what your children are doing.
- Self analysis 

---

Feel free to contribute to fix any problems, or to submit an issue!

Please note, this repo is for educational purposes only. No contributors, major or minor, are to fault for any actions done by this program.

Giacomo Lawrance – [@GiacomoLaw](https://twitter.com/GiacomoLaw) - [My website](https://about.me/giacomolaw)

Distributed under the MIT license. See [LICENSE](https://github.com/GiacomoLaw/Keylogger/blob/master/LICENSE.txt) for more information.
