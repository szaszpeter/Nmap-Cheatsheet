# Nmap Cheatsheet
An empty repo containing a list of useful Nmap Commands

## Installing Nmap on Linux

- `apt-get install nmap` - install nmap

## Scan a target

- `nmap <ip_address>` - scans a specified ip address
- `nmap <domain_name>` - scans the server behind the specified domain name



## Scan multiple targets

- `nmap 192.168.1.1-30` - scan all ip addresses between 192.168.1.1 and 192.168.1.30
- `nmap 192.168.1.*` - scan all the ip addresses from the 192.168.1. subnet


  
## Aggressive / Detailed scans

- `nmap -A <target>` - scans the target and displays detailed information like open ports, operating systems, traceroutes etc.
- `nmap --traceroute <target>` - scans the target and displays the traceroute used to connect. 
- `nmap -O <target>` - scans the target to find out the operating system running on it.
- `nmap -sV <target>` - scans the target to find out service versions.



## Different port options for scanning

- `nmap -F <target>` - only scan the popular ports of a target. Faster results will be obtained
- `nmap -p  20-25, 43, 88 <target>` - scan only the specified ports. can be a range or a specific port number.
- `nmap -p  http, mysql <target>` - scan ports by name
- `nmap -p- <target>` - scan all possible ports
- `nmap --open <target>` - only list open ports

## Writing results to a file

- `nmap -F -oN <destination> <target>` - writes the results in a regular textfile.
- `nmap -F -oX <destination> <target>` - writes the results in an XML file.

## Verbose scan

- `nmap -v <target>` - prints out logs while scanning.
