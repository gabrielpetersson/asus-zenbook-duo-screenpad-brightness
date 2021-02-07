# Why

With the latest Ubuntu 20, the brightness of the screenpad on duo computers is hard to keep at max brightness

# Usage

```
sp-brightness (0-1) # sets brightness once
sp-brightness-loop (0-1) # sets brightness every 5 sec (my ubuntu resets brightness randomly and everytime a program starts)
```
Run `sp-autostart` on reboot with cron or ubuntu autostart.

Run `screenpad 9` along with this. or just `sp-autostart` manually

# Install

Setup way #1 of setting brightness: https://github.com/Plippo/screenpad-tools

Clone this repo and make scripts executable:
`chmod -x bin/sp-x`

It will run the above script once and set the #1 way of changing brightness to max, and then have an inifinite loop setting the #2 way to max every 5 sec.
Run on autostart: `/path/to/project sb-autostart`

# Background

The screenpad brightness has 2 different ways of being changed.
My screenpad becomes dark everytime I start a application, and the ubuntu gui way of changing brightness is broken for it.
Although you can set the brightness programatically, the screenpad has it's own internal brightness mechanism as well,
which Plippo managed to mimic the windows behavior for chaning this here: https://github.com/Plippo/screenpad-tools

Not running the loop script at all time for me leads to ubuntu setting brightness to 0 randomly.

Tested for Ubuntu (Budgie) 20.04, Asus Pro Duo UX581 i9 10th gen variant
