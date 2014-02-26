# Gnome Alt Tab
----------------

Execute the following command below:

```bash
gsettings set org.gnome.desktop.wm.keybindings switch-windows "['<Alt>Tab']"
```

Note: If you get error GLib-GIO-Message: Using the 'memory' GSettings backend.  Your settings will not be saved or shared with other applications. Install dconf using yum and run again command. 

```bash
yum install dconf
```
