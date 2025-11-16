# forward

forward is a frontend to manage port forwarding rules with iptables.

It is similar to UFW, which is a frontend for firewall rules in iptables.


# How to use

Just clone this repository or download the forward script:
```sh
git clone https://github.com/lispydev/forward
cd forward
# or
wget https://raw.githubusercontent.com/lispydev/forward/refs/heads/master/forward
```

forward will track its own rules to manage them on its own:
```sh
# forward port 80 to a libvirt VM in the default NAT:
sudo ./forward add port 80 to 192.168.122.3:80
sudo ./forward list
sudo ./forward del port 80
```


# Roadmap

Todo:
- improve input validation
- add persistence
- package in distros for ease of install
- hide iptables commands
- automate tests

