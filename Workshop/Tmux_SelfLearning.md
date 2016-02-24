# Workshop
## Creating sessions
To start using tmux launch the following command that will create a tmux session named **_RandomName_**


** tmux new -s _RANDOM_NAME_**


Once inside the tmux session launch the **htop** command.


**htop**


## De-attaching & attaching to running sessions
De-attach from the session.


**Crtl+b d**


**NOTE:** **Crtl+b + command** is the way to interact with tmux. This key combination can be remaped

Now the tmux session is running in the background with the htop command running.

Let's list the running tmux sessions

**tmux ls**

Re-attach to **YOUR** session

**tmux a -t _RANDOM_NAME_**

The **htop** should be running

## Working with panes

### Create panes

#### Horizontal pane


**Crtl+b "**


#### Vertical pane


**Crtl+b %**


### Move between panes
This can be achieved using the cursor keys


**Ctrl+b _CURSOR_KEY_**


### Resize panes


**Ctrl+b Alt+_CURSOR_KEY_**


### Remove panes


**Ctrl+b d**

Or

**exit**


## Working with windows

### Create window


**Crtl+b c**

### Rename window

**Crtl+b ,**

Type the desired name

### Move between windows
This can be achieved selecting the desired window from a list or using a key combination

#### list windows

**Crtl+b w**

Will show all the windows from the current tmux session. To select a window just press the number or letter located near to the window's name

#### Move between windows using a key combination

**Ctrl+b _NameOrLetter_**


### Remove windows
Enter in the desired window and type

**Ctrl+d d**

Or

**exit**

## Synchronize panes
Very useful to launch the same command to several panes and/ir ssh session. **First of all ensure that in the current windows there are two or more panes.**

To enable the pane synchronization is necessary to use the "command" mode (similar to VI). To do this


**Ctrl+d :**


Then write:


**setw synchronize-panes**


At this moment all the command typed will be sent to all the panes on the current window. To disable the pane synchronization send the same command (togle on/off)


**Ctrl+d :**


Then write:


**setw synchronize-panes**


## Practice by yourself
For several minutes and get used to the new environment






























