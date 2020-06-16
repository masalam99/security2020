# Commands
---enable => from R> to R#
configure terminal {Config t} => R# to R#(Config)


## Configure IP of Routers
- R(Config)# int f0/0 
    - interface fasteathernet/Port
- R(Config-if)# ip address 192.168.1.1 255.255.255.0
- R(Config-if)# no shutdown (= no shut)
- R(Config-if)# exit

## Configure Telnet 
- R(Config)# line vty 0 4
- R(Config-line)# password 123
- R(Config-line)# login

## Sessions of Telnet 
- R# show sessions 
- R# telnet 192.168.1.1 => R2
- R2# do any Thing
- to keep session open and return to the base router
    - Ctrl+ Shift + 6 => x 
- R# resume 2 
- R2# do any thing 
- R# disconnect 2 
- or exit from connection

## Access-List standard
- R(Config)# access-list 1 deny host 192.168.1.2
- R(Config)# access-list 1 permit any