# PyOS
A Linux-based OS that does just Python. Intended for small devices such as the Raspberry Pi, CHIP, VoCore, and the like. This should make developing Python for these boards as easy as dropping a .py file onto the SD card, while also providing access to important OS features.

This should make Python development on a Linux-capable SBC or embedded device as easy as using MicroPython, but with full access the all of Python, its libraries, and its debugger.

Key features:
* Looks for a file `main.py` and `boot.py` on startup, and runs those.
* Everything that the user wants to do should be able to be done via Python.
* Console access provides an interactive ipython prompt.

The following OS operations will need to have translated into Python (or libs found)
* Network configuration and information, including wired and wireless
* Power functionality (sleep, reset, poweroff)
* Time functionality, including ntp
* Watchdog
* SSH configuration - remote debugging will be done via ssh
* Recurring tasks - this could be an abstraction of cron, or using another task queue such as Celery

Possible inclusions:
* ipython notebook interface (see Pynq)

## Resources
* Micropython libraries: https://docs.micropython.org/en/latest/pyboard/library/index.html#micropython-specific-libraries
* Pynq linux implementation: http://www.pynq.io/home.html
* Python network configuration: https://github.com/rlisagor/pynetlinux/tree/master/pynetlinux
