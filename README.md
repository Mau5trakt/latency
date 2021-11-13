# Latency
CLI that sends a IMPC package to the Google Public DNS IPv4 and show the time in miliseconds that this took<br>
<img src="https://img.shields.io/badge/Shell_Script-121011?style=for-the-badge&logo=gnu-bash&logoColor=white">
<img src="https://img.shields.io/badge/Linux-FCC624?style=for-the-badge&logo=linux&logoColor=black">
<img src="https://img.shields.io/badge/Arch_Linux-1793D1?style=for-the-badge&logo=arch-linux&logoColor=white">
<p>
<h2> Getting started </h2>
latency was made it to be a widget for Qtile that shows only the ms of latency to have a control of it

<h3> how does it works?</h3>
works with the command ping (in linux) and transform the output to only have the miliseconds of latency 

<b> ping -c 10 -A 8.8.8.8 output:</b> <br>

PING 8.8.8.8 (8.8.8.8) 56(84) bytes of data. <br>
64 bytes from 8.8.8.8: icmp_seq=1 ttl=111 time=60.1 ms<br>
64 bytes from 8.8.8.8: icmp_seq=2 ttl=111 time=58.5 ms<br>
64 bytes from 8.8.8.8: icmp_seq=3 ttl=111 time=56.7 ms<br>
64 bytes from 8.8.8.8: icmp_seq=4 ttl=111 time=54.8 ms<br>
64 bytes from 8.8.8.8: icmp_seq=5 ttl=111 time=56.9 ms<br>
64 bytes from 8.8.8.8: icmp_seq=6 ttl=111 time=54.9 ms<br>
64 bytes from 8.8.8.8: icmp_seq=7 ttl=111 time=56.9 ms<br>
64 bytes from 8.8.8.8: icmp_seq=8 ttl=111 time=65.1 ms<br>
64 bytes from 8.8.8.8: icmp_seq=9 ttl=111 time=54.9 ms<br>
64 bytes from 8.8.8.8: icmp_seq=10 ttl=111 time=55.1 ms<br>
<br>
--- 8.8.8.8 ping statistics ---<br>
10 packets transmitted, 10 received, 0% packet loss, time 530ms<br>
rtt min/avg/max/mdev = 54.812/57.408/65.059/3.038 ms, pipe 2, ipg/ewma 58.850/58.020 ms<br>
<br>

<b> latency output: </b>
<br>
59.8 ms<br>
58.0 ms<br>
58.9 ms<br>
60.2 ms<br>
62.2 ms<br>
57.5 ms<br>
61.4 ms<br>
<br>

to get this see comando.txt in the tests folder 

<h2>Build with</h2>

* [Bash](https://www.gnu.org/software/bash/)

<h2> Usage </h2>
clone this into your repos file or in your personal file,<br>   


   ```sh
   git clone https://github.com/Mau5trakt/latency.git
   ````

then execute pwd 

in my case the output is 
/home/kubz/develop/latency

this output you have to put at the bottom of the .bashrc file in the user directory

```sh
   PATH="$PATH:/home/kubz/develop/latency"
   ````
in my case this is my route, make sure you are in the route with the latency file

then save the .bashrc 

in case that youren't using the default shell (in my case im using oh my fish shell)
you have to write it in the .config file of you bash interpreter 
 
in my case i add  

set PATH "$PATH:/home/kubz/develop/latency"

in the end of the file. 


<h2>Usage </h2>

$ latency 

to exit Ctrl + C

<>Modify the program</h2>
in latency/ do the following command: 

```sh
   mv latency latency.sh
   ````

this is bc if i have latency.sh to use it i had to write latency.sh instead only latency 

and then modify it. 

<b> things to modify </b>

the address to ping in latency is by default 8.8.8.8 you can put here the host you like. 

<h2> in the future? </h2>
well i did this bc i like to see the ping but is annoying putting "ping 8.8.8.8 -c 10" every time i want it 
and i want to put this in a widget of Qtile but i think that i can put a -h flag and in there put the host what 
i want to ping and see the latency (maybe i will see the latency between my pc and the server of a game or a service)
idk 


</p>
