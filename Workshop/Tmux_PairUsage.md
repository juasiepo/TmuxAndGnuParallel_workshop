# Workshop Pair Usage

## Connect to the remote server

**ssh usuario@workshop1.eltorete.com**

## Connect to the existing session

**tmux a -t workshop**

## Wait till the session is configured
Pay attention how the session is configured

## Bonus Track

### Nested tmux session
Have a look to the tmux.conf file located on Conf/tmux.conf

Launch a tmux session with the -f tmux.conf modifier

**tmux -f Conf/tmux.conf

launch ssh session against one of the test servers

**ssh usuario@workshop1.eltorete.com**

launch tmux again

**tmux**

*What happened with the tmux bar?
Why?*


#NOTE: Pairing a tmux session with a shared account is the simplest way but not the safest way. There is another option to pair using separate accounts and sockets. (out of the scope of this workshop)
