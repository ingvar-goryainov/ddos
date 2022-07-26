# ddos-attacks
Setup two docker containers:
1. attacker container - there you need to write scripts that will implement 6 attacks (UDP Flood, ICMP flood, HTTP flood, Slowloris, SYN flood,  Ping of Death)
2. Defender container - ubuntu & nginx with simple website
3. Try to implement protection on Defender container
4. Launch attacker scripts and examine you protection


## Run Example
```bash
$ docker-compose up
$ docker-compose run kali bash
$ apt-get install hping3 siege
$ hping3 --rand-source -2 --fast -V -D -c 100 protected
$ siege -b  -c100 -v -t30s protected
```