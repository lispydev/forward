# forward

forward is a cli frontend to manage port forwarding rules with iptables.

It works similarly to UFW, the uncomplicated firewall.


# How to use

Just clone this repository or download the forward script:
```sh
git clone https://github.com/lispydev/forward
cd forward
# or
wget https://raw.githubusercontent.com/lispydev/forward/refs/heads/master/forward
```

In order to have forward globally available, you can add it to `/usr/local/bin/`:
```sh
sudo mv ./forward /usr/bin/local/
```

forward will track its own rules to manage them on its own:
```sh
sudo forward start

# forward port 80 to a VM:
sudo forward add port 80 to 192.168.122.3:80
sudo forward list
sudo forward del port 80

sudo forward stop
```

Port forwarding rules will be saved in ports.json. Currently, this file is created and read in the current working directory when running forward.


# Roadmap

Todo:
- package in distros for ease of install
- automate tests
- process rule deletions without reloading other rules

