#GNU Parallel

## Working in serial
Create a temporal folder


**mkdir gnuparallel**


Create a tmux sesion

**tmux new -s gnuparallel**

Create 100 files with 5M size


**time for i in `seq 1 100`; do fallocate -l 5M test$i.img; done**


Compress all the files 


**time for i in `ls *.img`; do gzip -9 $i; done**

Check the times given by the time command

## Working in parallel
Create a temporal folder


**mkdir gnuparallel**


Create a tmux sesion

**tmux new -s gnuparallel**

Create 100 files with 5M size


**time seq 1 100 |parallel fallocate -l 10M test{}.img**


Compress all the files 


**time ls *.img |parallel gzip -9 {}**

Check the times given by the time command

