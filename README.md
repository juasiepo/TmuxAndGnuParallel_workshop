# Tmux & Gnu Parallel shaken, not stirred workshop


##Overview:

Workshop files for the  Tmux & Gnu Parallel shaken, not stirred workshop hosted by the AlicanteTech meetup group.

http://www.meetup.com/es-ES/AlicanteTech/events/225369345/

## Tmux Installation:

###Linux:

```bash
apt-get install tmux (deb based OS)
```
```bash
yum install tmux (rpm based OS)
```

###Mac:

```bash
brew install tmux (Homebrew)
```
```bash
port install tmux (Mac Ports)
```

###Windows:

Download Cygwin depending your OS architecture:

* [https://cygwin.com/setup-x86.exe] *(32 bits version)*
* [https://cygwin.com/setup-x86_64.exe] *(64 bits version)*

Install Cygwin launching the installation program from a MS-DOS shell: **setup-x86.exe -B**

```msdos
setup-x86.exe -B
```

Then install the tmux package using **Cygwin's GUI**


## GNU Parallel Installation:

###Linux:

```bash
apt-get install parallel (deb based OS)
```
```bash
yum install parallel (rpm based OS)
```

###Mac:

```bash
brew install parallel (Homebrew)
```

###Windows:

Download Cygwin depending your OS architecture:

* [32 bits version](https://cygwin.com/setup-x86.exe)
* [64 bits version](https://cygwin.com/setup-x86_64.exe)

Install Cygwin launching the installation program from a MS-DOS shell:

```msdos
setup-x86.exe -B
```

Then install the wget or curl package using **Cygwin's GUI**

Finally launch the Cygwin console an then 

```bash
(wget -O - pi.dk/3 || curl pi.dk/3/ || fetch -o - http://pi.dk/3) | bash
```

Don't forget to export SHELL=cmd.exe otherwise not -j nor multiprocess support will be available (by default cygwin will try to use sh.exe.. which won't work well on Win32 env.) 

```bash
export SHELL=cmd.exe
```













Files:
---------

* **Slides/PentahoWorkshopPresentation.odp** LibreOffice impress presentation

* **diputados.json** test data from http://api.quehacenlosdiputados.net/iniciativas