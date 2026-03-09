# Shell scripts for CachyOS

Here you will find a few useful little helpers for **CachyOS**.

> [!NOTE]
> If you don't know how to set up and use shell scripts in general, read the brief [instructions](#how-to-set-up-and-use-shell-scripts) at the bottom of this page.


## cleanup-shader-cache.sh

**What this shell script does** 
This script cleans up the locally generated shader cache for all local user accounts under /home/. It uses the various directory paths where shader caches for NVIDIA, Vulkan, Mesa and Steam are usually stored. A summary is then displayed to the user.

**What is the shader cache?** 
When you start a game or program, your graphics card has to create small calculation programs (called shaders) that determine how images are displayed on the screen - e.g., light, shadows, or reflections. Since this creation takes time, the finished results are stored in a temporary memory - the shader cache. The next time you start the game or program, the graphics card can then access these stored results instead of recalculating everything. This ensures faster loading times and less stuttering.

**Why and when should I delete the shader cache?** 
A new graphics card driver often "communicates" with the hardware slightly differently than the old one. The shaders stored in the cache are then no longer fully compatible with the new driver – like instructions written for an older version of a device. This can lead to graphics errors, crashes, or poorer performance. This is particularly relevant in Linux because the system often does not automatically recognize and discard old shader caches as obsolete, as Windows drivers more frequently do. It is therefore recommended to manually delete the cache after an update – the shader cache will simply be rebuilt and adjusted the next time the game or program is started.


## How to set up and use shell scripts

1. If necessary, create a folder for your scripts in your home directory, e.g. /home/*YOURUSERNAME*/.local/bin/
```shell
mkdir -p ~/.local/bin/
```
2. Download the script file from the [GitHub repository](https://github.com/LoopSkyworker/linux_cachyos_stuff/tree/main/shell-scripts) via a web browser or via console: 
```shell
curl -fL https://github.com/LoopSkyworker/linux_cachyos_stuff/blob/main/shell-scripts/SCRIPTNAME.sh -o ~/.local/bin/
```
3. Make the script executable: 
```shell
chmod +x ~/.local/bin/SCRIPTNAME.sh
```

## License

See the [LICENSE](LICENSE.md) file for license rights and limitations (MIT).


## Disclaimer

This software is provided "as is" without any warranty of any kind.