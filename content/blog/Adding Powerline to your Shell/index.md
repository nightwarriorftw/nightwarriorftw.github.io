---

title: Adding powerline to your Shell 
date: "2019-03-21T17:12:33.962Z"
---

This is how your current terminal looks like 
<img src="terminal-without-powerline.png">
Now with some awesome tricks you can change it too
<img src="terminal-with-powerline.jpeg">

### Step 1

Install `font-awesome` and `powerline`.
For Debian based operating system use the following command
```
sudo apt install powerline fonts-powerline
```
This command might be different for different flavours of Linux based Operating system

### Step 2

Change the configurations of your `.bashrc`.
Open the terminal and type `nano ~/.bashrc` or open your `.bashrc` in any text editor.
Add the following lines
```
if [ -f `which powerline-daemon` ]; then
   powerline-daemon -q
   POWERLINE_BASH_CONTINUATION=1
   POWERLINE_BASH_SELECT=1
   . /usr/share/powerline/bindings/bash/powerline.sh
fi
```
Make sure the last line in the above is the path where the `powerline` tool is installed. It might be different for different operating system. Set this path according to your operating system.

### Step 3

Source your `.bashrc` file in order to add changes.
```
source ~/.bashrc
```
