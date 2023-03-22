# Why

The brightness of both screens on the Asus Pro Duo series is completely messed up on linux using nvidia drivers. This maxes the brightness on both screens 

# Install

For some reason there are 2 sources that affect the brightness of the screen. We need to set both to max by:
1) setup screenpad-tools: https://github.com/Plippo/screenpad-tools, the first source can be set to max by running `screenpad 9`

2) clone this repo and make scripts executable:
`chmod -x bin/<filename>`

# Usage

```
sp-brightness (0-1) # sets brightness once
sp-brightness-loop (0-1) # sets brightness every 5 sec (my screen resets brightness randomly)
/path/to/project sb-autostart # runs both my script & `screenpad 9` (needs sudo)
```
Run the `sp-autostart` script on startup with e.g. ubuntu autostart to not have to run this manually every time.

# Background

The screenpad brightness has 2 different ways of being changed.
My screenpad becomes dark everytime I start a application, and the Ubuntu Gui is broken duo laptops.
Although you can set the brightness programatically, the screenpad has it's own internal brightness mechanism as well,
which Plippo managed to mimic the windows behavior for chaning this here: https://github.com/Plippo/screenpad-tools

Tested for Ubuntu (Budgie) 20.04, Asus Pro Duo UX581 i9 10th gen variant
