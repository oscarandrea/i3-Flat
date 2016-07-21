# **i3-Flat**

*INCOMPLETE !!!*

beautiful and minimal ambiance for i3

## Installation 

### i3-Flat require following dependecies:

[i3-gaps] (https://github.com/Airblader/i3) 
[i3status] (https://github.com/i3/i3status) 
[conky] (https://github.com/brndnmtthws/conky)
[rxvt-unicode] (urxvt) (http://dist.schmorp.de/rxvt-unicode) 
[urxvt-pearls] (http://www.github.com/muennich/urxvt-perls)
[compton] (https://github.com/chjj/compton)
[feh] (http://feh.finalrewind.org)


#optional dependency are
[vim] (https://github.com/vim/vim)
[amix/vimrc] (https://github.com/amix/vimrc) for vimrc and some plugin

[nano] (https://www.nano-editor.org/download.php)
[figlet] (http://www.figlet.org/) for ascii text on terminal


##pacman
pacman -S feh urxvt-perls rxvt-unicode conky compton 

#optional
figlet vim nano 


## Bar
Add following line 

ibar {
    #launch json wrapper more info on: https://i3wm.org/docs/user-contributed/conky-i3bar.html
    status_command $HOME/conky-wrapper-i3
	position top

  colors {
    separator #268bd2
    background #1C1C1C
    statusline #839496
    focused_workspace #87D7FF #1C1C1C #87D7FF
    active_workspace #fdf6e3 #1C1C1C #fdf6e3
    inactive_workspace #D7D787 #1C1C1C #D7D787 
    urgent_workspace #d33682 #d33682 #fdf6e3
  }
}

client.focused #1C1C1C #1C1C1C #60B48A #1C1C1C 
client.focused_inactive #1C1C1C #1C1C1C #eee8d5 #1C1C1C
client.unfocused #1C1C1C #1C1C1C #93a1a1 #1C1C1C
client.urgent #d33682 #d33682 #fdf6e3 #dc322f

#palette
#backgroud  cyan    green
#1C1C1C   #D7D787  #87D7FF

#internal gaps border
gaps inner 10

#external gaps border
gaps outer 15

#border propriety for new windows
new_window pixel 3

#default fonts for windows and bar (if you don't override in .conkyrc)
font pango:Monospace 10.5

#disable border for urxvt windows 
for_window [instance=urxvt] border none

#script for launch urxvt in i3 with support utf-8
bindsym $mod+Return exec urxvtf


#i prefer use xinitrc

#compositor
compton -b

#load config
xrdb -merge $HOME/Xresources-urxvt

#set your wallpaper
feh --bg-fill $HOME/Immagini/flat03.jpg

#setting keyboard 
setxkbmap it

#launch wm
i3
####################################


