## No Credentials
### Scan Network
- `nxc smb <ip_range>`
- `nmap -sP -p <ip>`
- `nmap -Pn -sV --top-ports 50 --open <ip>`
- `nmap -Pn --script smb-vuln* -p139,445 <ip>`
- `nmap -Pn -sC -sV -oA <output> <ip>`
- `nmap -Pn -sC -sV -p- -oA <output> <ip>`
- `nmap -sU -sC -sV -oA <output> <ip>`

➔ Vulnerable host

## Find DC IP
- `nmcli dev show <interface>`
- `nslookup -type=SRV _ldap._tcp.dc._msdcs.<domain>`
- `nmap -p 88 --open <ip_range>`

## Zone Transfer
- `dig axfr <domain_name> @<name_server>`

## Anonymous & Guest Access on SMB Shares
- `nxc smb <ip_range> -u '' -p ''`
- `nxc smb <ip_range> -u 'a' -p ''`
- `enum4linux-ng.py -a -u '' -p '' <ip>`
- `smbclient -U '%' -L //<ip>`

## Enumerate LDAP
- `nmap -n -sV --script 'ldap*' and not brute -p 389 <dc_ip>`
- `ldapsearch -x -H <dc_ip> -s base`

➔ Username
