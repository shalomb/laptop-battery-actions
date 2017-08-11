# laptop-battery-actions

A script that reacts to `acpid` events and does the following

* Set backlight brightness to the battery level - decreasing brightness is a
  good battery-level indicator and a really dim screen means you ought to plug
  in sometime soon.
* Invokes `tlp` and `pm-powersave` powersave configurations when battery is 
  discharging or to optimized otherwise.
* Hibernates the laptop on a critically low battery level.

## Installation

    sudo -E ./INIT

## Configuration

See `/etc/default/laptop-battery-actions` for options.

After changes to the defaults file, make sure to reload the `acpid` service.

    service acpid restart

## TODO

* React to lid events and suspend to disk (as opposed to RAM) if under some 
  threshold.

