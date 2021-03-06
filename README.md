# Mpv Filenavigator  
File navigator for mpv media player. Currently works on Linux and MacOS, relies on default unix commands cd, pwd, sort, test and ls. Edit the settings variable in the lua file to change defaults and to add favorite paths. Big thanks to [SteveJobzniak](https://github.com/SteveJobzniak) for contributing MacOS compability and more reliable features, check out his awesome lua scripts in [mpv-tools](https://github.com/SteveJobzniak/mpv-tools).

#### Keybinds  
- __navigator (Alt+f)__ Activate script. When using dynamic keys this will need to be invoked to register keybindings.
- __nav-up nav-down (up/down)__ cursor up/down
- __nav-back nav-forward (left, right)__ directory back/forward, incase of file append to playlist
- __nav-undo (Backspace)__ undo last playlist append(just removes last entry in playlist)
- __nav-open (Enter)__ open directory or file with mpv, same as `mpv /path/to/dir-or-file`, replaces playlist
- __nav-favorites (f)__ cycle between favorite directories, edit settings to setup

On default dynamic keys are active which means that other binds than navigator(Alt+f) will only be active after activating the script with navigator keybind and until the osd timeouts. Dynamic keybindings will only override keys while they are active. Dynamic setting toggle can be changed in lua settings variable. All keybinds can be changed in input.conf with `KEY script-binding keybind-name` ex. `K scipt-binding nav-favorites`.  Below is a list of all keybindings for copy pasting to input.conf:  
```
#Filenavigator keybindings
Alt+f script-binding navigator  
#Dynamic keybindings
f script-binding nav-favorites
UP script-binding nav-up  
DOWN script-binding nav-down  
LEFT script-binding nav-back  
RIGHT script-binding nav-forward  
BS script-binding nav-undo  
ENTER script-binding nav-open  
```
![alt text](https://giant.gfycat.com/DisfiguredBlindAmethystinepython.gif "Screenshot")

#### My other mpv scripts
- [collection of scripts](https://github.com/donmaiq/mpv-scripts)
