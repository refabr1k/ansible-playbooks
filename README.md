# ansible-playbooks
Ansible playbooks to setup initial configurations, install various utilities, and security tools to localhost.

## Playbooks
Forked from https://github.com/JohnHammond/ansible-playbooks 

Modified for the Ubuntu focal 20.04

## Testing
This has been tested on focal 20.04.

### Dependencies
Packages to be installed prior to running the playbooks.

```bash
$ apt update
$ apt -y install python-apt ansible
```
Optionally, many of these tools can be installed by the `forensics-all` package described in [Debian Forensics Environment - essential components](https://packages.debian.org/sid/forensics-all).

### Usage
Perform a dry run:

```bash
$ sudo ansible-playbook play_apt.yml --check
```

List tasks or tags:
```bash
$ sudo ansible-playbook play_apt.yml --list-tasks
```

Install or skip specific tasks:
```bash
$ sudo ansible-playbook play_apt.yml --tags "deb-utils,pip3-sec"
$ sudo ansible-playbook play_apt.yml --skip-tags "deb-sec,pip-sec"
```

Run playbook and all install tools to localhost:

```bash
$ sudo ansible-playbook play_apt.yml --tags "deb-utils,kismet,deb-sec,impacket,wpscan,dirsearch,gobuster,responder,wordlists"
```

### Whats included?

Pentesting tools:
  - nbtscan
  - samba-common-bin
  - smbclient
  - smbmap
  - polenum
  - ldap-utils
  - samba
  - cifs-utils
  - python-scapy
  - python3-scapy
  - scanssh
  - zenmap
  - sqlmap
  - dnsrecon
  - ncrack
  - onesixtyone
  - cewl
  - john
  - fcrackzip
  - pdfcrack
  - hashcat
  - hydra
  - hashid
  - crunch
  - recon-ng
  - aircrack-ng
  - airgraph-ng
  - wireshark
  - tshark
  - tcpflow
  - hunt
  - mdbtools
  - pst-utils
  - p7zip-full
  - libimage-exiftool-perl
  - steghide
  - zbar-tools 
  - beef
  - volatility
  - binwalk
  - wpscan
  - kismet
  - responder
  - dirsearch
  - gobuster

Other tools:
  - git
  - ftp
  - jq
  - telnet
  - netcat
  - socat
  - rdesktop
  - tmux
  - vim
  - tree
  - golang-go
  - nmap
  - docker.io
  - speedtest-cli
  - mupdf-tools
  - whois
  - rkhunter
  - clamav
  - clamav-daemon
  - dmg2img
  - lynis
  - php
  - terminator
