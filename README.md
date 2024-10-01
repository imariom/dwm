#+imariom-dwm

* Table of Contents :toc:
- [[#about-dwm][About Suckless Dwm]]
  - [[#the-patches-i-added-to-this-build-include][The patches I added to this build include:]]
  - [[#the-dependencies-for-dwm-distrotube-include][The dependencies for imariom-dwm include:]]
- [[#installing-imariom-dwm][Installing imariom-dwm]]
- [[#my-keybindings][Keybindings]]
  - [[#main-keybindings][Main keybindings]]
  - [[#application-controls][Application controls]]

* What is DWM?
#+CAPTION: dmenu-distrotube
#+ATTR_HTML: :alt imariom-dwm :title imariom-dwm :align left
[[https://github.com/imariom/dotfiles/.screenshots/imariom-dwm-thumb.png]]

Dwm is an exceptionally fast, lightweight, and dynamic window manager for X, developed by the talented team at suckless.org. This build is my personal version of dwm, where I’ve applied several patches to enhance its functionality and usability, making it more 'sensible' while maintaining its minimalist approach, rather than strictly adhering to the 'suckless' philosophy.

** Patches added to this build include:
+ floatrules (setting the status bar width and floating coordinates)
+ statuspadding (horizontal and vertical padding in the status bar are now configurable options)
+ attachaside (new clients appear in the stack rather than as the master)
+ uselessgap (adding gaps when more than one window)
+ rotatestack (moves a window through the stack, in either direction)

** The dependencies for imariom-dwm include:
+ ttf-inconsolata-nerd (you can substitute it with your preferred nerd font family)
+ ttf-nerd-fonts-symbols
+ Alacritty
+ rofi

Also, you will need to add the following from the AUR:
+ https://aur.archlinux.org/packages/libxft-bgra/ (needed for colored fonts and emojis)

* Installing imariom-dwm
Download the source code from this repository or use a git clone:

#+begin_example
git clone https://gitlab.com/imariom/imariom-dwm.git
cd imariom-dwm
sudo make clean install
#+end_example

This build has only been tested on Arch Linux However, you are welcome to test it on your own system, and feel free to modify or customize it as needed. Your feedback and contributions are highly appreciated as we continue refining the project.

=NOTE:=Installing imariom-dwm will overwrite your existing dwm installation.

* Keybindings
The MODKEY is set to the Super key (aka the Windows key).

** Main keybindings

| Keybinding              | Action                                                       |
|-------------------------+--------------------------------------------------------------|
| MODKEY + RETURN         | opens terminal (alacritty but can be easily changed)         |
| MODKEY + SHIFT + RETURN | opens run launcher (dmenu but can be changed)                |
| MODKEY + SHIFT + c      | closes window with focus                                     |
| MODKEY + SHIFT + r      | restarts dwm                                                 |
| MODKEY + SHIFT + q      | quits dwm                                                    |
| MODKEY + b              | hides the bar                                                |
| MODKEY + 1-9            | switch focus to workspace (1-9)                              |
| MODKEY + SHIFT + 1-9    | send focused window to workspace (1-9)                       |
| MODKEY + j              | focus stack +1 (switches focus between windows in the stack) |
| MODKEY + k              | focus stack -1 (switches focus between windows in the stack) |
| MODKEY + SHIFT + j      | rotate stack +1 (rotates the windows in the stack)           |
| MODKEY + SHIFT + k      | rotate stack -1 (rotates the windows in the stack)           |
| MODKEY + h              | setmfact -0.05 (expands size of window)                      |
| MODKEY + l              | setmfact +0.05 (shrinks size of window)                      |
| MODKEY + .              | focusmon +1 (switches focus next monitors)                   |
| MODKEY + ,              | focusmon -1 (switches focus to prev monitors)                |

** Application controls

| Keybinding       | Action                                                                       |
|------------------+------------------------------------------------------------------------------|
| MODKEY + ALT + b | open Brave browser                                                           |
| MODKEY + ALT + c | open Visual Studio Code                                                      |
| MODKEY + ALT + s | open Spotify                                                                 |
| MODKEY + ALT + m | open [mailspring](https://github.com/Foundry376/Mailspring)                  |
| MODKEY + ALT + f | open [Thunar (Thunar)](https://wiki.archlinux.org/title/Thunar) |


