# Why

The brightness of both screens on the Asus Pro Duo series is completely messsed up on linux, especially using nvidia drivers. This maxes the brightness on both screens 

# Usage

```
sp-brightness (0-1) # sets brightness once
sp-brightness-loop (0-1) # sets brightness every 5 sec (my screen resets brightness randomly)
/path/to/project sb-autostart # run this on autostart. runs loops
```
Run `sp-autostart` on reboot with cron or ubuntu autostart.

Run `screenpad 9` along with this. or just `sp-autostart` manually

# Install

We need to control the brightness in 2 ways to ensure maximum brightness:
First, setup screenpad-tools: https://github.com/Plippo/screenpad-tools

Secondly, clone this repo and make scripts executable:
`chmod -x bin/<filename>`


# Background

The screenpad brightness has 2 different ways of being changed.
My screenpad becomes dark everytime I start a application, and the ubuntu gui way of changing brightness is broken for it.
Although you can set the brightness programatically, the screenpad has it's own internal brightness mechanism as well,
which Plippo managed to mimic the windows behavior for chaning this here: https://github.com/Plippo/screenpad-tools

Not running the loop script at all time for me leads to ubuntu setting brightness to 0 randomly.

Tested for Ubuntu (Budgie) 20.04, Asus Pro Duo UX581 i9 10th gen variant
