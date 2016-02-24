#Tasks

# Previous the workshop
1. Create 2 servers on distants CPD
2. Create user **usuario** for tests
3. Configure the DNS name resolution
3. Install the following  tools:

**apt-get tmux wget git htop parallel vim lighttpd iotop iftop**

# During the workshop
1. Connect to the server
2. Create the pair session
3. Create several windows (1 for pair programming & 1 for pair monitoring)

**ssh usuario@workshop1.eltorete.com**

**tmux new -s workshop**

Create 3 windows and rename them properly (pair programming & pair monitoring & pair administering)

##Pair programing:

clone the repository in one pane and vi one of the files

**git clone https://github.com/juasiepo/TmuxAndGnuParallel_workshop.git**

Create a new pane and launch

**watch -n 1 "git status"**

Create a new pane and do some git operations git commit, git add, git branch, etc

##Pair monitoring:

Create a new pane and tail the log file

**tail -f /var/log/lighttpd.log**

Create a new pane to start/stop the daemon

**/etc/init.d/lighttpd start/stop**

Create a new pane to test the web server

**lynx localhost**

##Pair administering

Create a new pane and connect to one of the servers

**ssh usuario@workshop1.eltorete.com**

Create a new pane and connect to the other server

**ssh usuario@workshop2.eltorete.com**

Synchronize both panes

**Ctrl+b :**

**setw synchronize-panes**

launch a "synchronized" grep on the lighttpd logs in both servers

**grep "X.X.X.X" /var/log/lighttpd.log**