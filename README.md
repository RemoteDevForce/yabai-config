# yabai-config
Resources &amp; Configs for Karabiner, Yabai, Skhd, Alfred, Hammerspoon, Limelight, &amp; Stackline

I followed this video and other related videos/configs to get to this. I heavily altered the final config for skhd to my liking.

https://www.youtube.com/watch?v=JL1lz77YbUE

A list of shortcuts for Yabai & Stackline via Skhd can be found [here](SHORTCUTS.md)

I've also just added a screenshot of [iterm shortcuts](iterm-shortcuts.png), I added split H/V shortcuts.

Regarding the video, I have more details below on setting this all up below.

I followed the video but run into some issues. I did the no SAPI route and I'm on monetary M1 Mac.

At each point when you're installing something, copy the configs here in the appropriate places (mainly under `~/.config`).

Find your favorite mp3 of a soundbyte that you think is funny and replace the `fail.mp3` with your own. In the karabiner config file, `insert` action with the location of where you put this file. Now when you hit `insert` it will play your soundbyte.

Put the `window-focus-on-destroy.sh` file somewhere and replace `yabairc` location with the location of your file. Make it executable.

Setup karabiner first (watch his part 1 & 2 videos) - make sure you edit config with vscode to ensure you don't mess up the json otherwise it won't load anything - also took out the CMD+W cause I use that to close browser tabs and don't run into the fat finger issue of trying to hit CMD+S - when you install, there is a step to go into safe mode, note that when you hold shift after selecting your hard drive, you must wait for it to say "Safe Mode Continue" before you click it, that tripped me up. also karabiner binaries didn't show in my accessibility security settings until I did that and restarted computer. I changed The Toggle caps_lock rule from “to” to “to_if_held_down” so I could avoid cap lock in rare cases where I hit both. Toggle Alfred has a bug I think, change modifier from left_command to left_option and now instead of spotlight, Alfred should open. For “Double tap cmd q closesapps” just make sure you tap qq quick enough. I didn’t add the simple config shown in the video for left_option->right_option cause I wasn’t a fan of the shift left/right one word (I kept jumping words as I was typing) so I changed the rule to left_option + j or k for left/right one word. Removed the vim navigation part cause I don’t live in the stoneage, lol just giving y’all vim loves a hard time, I use it on servers. I also added my open O+ actions for opening my most used apps which differs. 

Installed Alfred, bought power pack but pause is doing something with brightness for some reason and doesn't trigger my workflow to sleep computer, found out there was a typo in the Karabiner config, change osacript to osascript - might have been just a copy paste issue on my side but it is working now. You have to set that workflow up in Alfred but its pretty straight forward.

installed yabai via brew, did the start to autoload it on startup but had to restart computer before yabai actually started working
I changed a few things in yabairc for floating windows, I term isn't iterm2 anymore and wanted iMessage to float. Again all my configs are available in the link above.

DO NOT INSTALL LIMELIGHT SEPARATELY, tried that and limelight kept segfaulting, instead it is built into yabai so I edited the config. See my yabairc file in the link. Even though I didn't disable SIP, THIS WORKS and won't segfault! no need for the limelight start/kill in config

I only copied the window-focus-on-destroy.sh script and change the yabairc to that path, his config has his username so it won't work

Installed skhd via brew but brew was failing, after restart and brew update, it worked, not totally sure why. Was going to do the manual install but was confused on how to get the program to autostart/security permissions so def use the homebrew route.

Installed hammerspoon, stackline and updated configs to get that working.

Enjoy! I printed the shortcuts and put them on my wall above my keyboard to get the hang of using it.

## TODO
Would like to figure out how to move a window in split fasion without dragging the window. Hard to explain but example would be lets say you have 3 windows side-by-side but taking a window and placing under/above a window next to it rather than just moving the window. I can achive it but dargging with my mouse below a window but theres gotta be a way to do that via skhd, PRs are welcome!
