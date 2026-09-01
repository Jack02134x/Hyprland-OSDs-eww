
# Hyprland OSDs   

In this repo i created very minimal volume and brightness OSDs for Hyprland using eww. I made it becuase I had quite the trouble finding some premade ones.


# Installation

```
git clone https://github.com/Jack02134x/Hyprland-OSDs-eww.git
mkdir ~/.config/eww
cd Hyprland-OSDs-eww
cp -r scripts/ eww.scss eww.yuck ~/.config/eww
```

*Then inside hyprland.lua config*

```
# FOR VOLUME --------

hl.bind("XF86AudioRaiseVolume", hl.dsp.exec_cmd("~/.config/eww/scripts/volume.sh up"), { locked = true, repeating = true  }) 
hl.bind("XF86AudioLowerVolume", hl.dsp.exec_cmd("~/.config/eww/scripts/volume.sh down"), { locked = true, repeating = true  }) 
hl.bind("XF86AudioMute", hl.dsp.exec_cmd("~/.config/eww/scripts/volume.sh mute"), { locked = true })

# FOR BRIGHTNESS --------

hl.bind("XF86MonBrightnessUp",   hl.dsp.exec_cmd("~/.config/eww/scripts/brightness.sh up"), { locked = true, repeating = true })
hl.bind("XF86MonBrightnessDown", hl.dsp.exec_cmd("~/.config/eww/scripts/brightness.sh down"),  { locked = true, repeating = true })
```

