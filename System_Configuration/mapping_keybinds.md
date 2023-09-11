# Mapping Keybindings

[xcape repo](https://github.com/alols/xcape)

[Ask Ubuntu Threat](https://askubuntu.com/questions/1220552/how-do-i-set-caps-to-both-control-and-escape-in-ubuntu-gnome)

```
# make CapsLock behave like Ctrl:
setxkbmap -option ctrl:nocaps
# make short-pressed Ctrl behave like Escape:
xcape -e 'Control_L=Escape'
```
