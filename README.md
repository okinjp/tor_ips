# tor_ips
Tor exit node IP addresses (Generate from metrics.torproject.org)
## Type(s)
Files with the suffix _v4 or _v6 are lists of only IPv4 or IPv6 addresses.
### General
#### tor_ips.txt
Simply lists IP addresses separated by line breaks

##### Example
```
101.99.84.87
101.99.84.87
2001:1620:51a1:0:8aae:ddff:fe61:8ccc
...
```

### Nginx config
#### Usage
```
location / {
    include allow-tor_ips.conf;
}
```
#### allow-tor_ips.conf
"allow" list of IP addresses separated by semicolons.
##### Example
```
allow 101.99.84.87;
allow 101.99.84.87;
allow 2001:1620:51a1:0:8aae:ddff:fe61:8ccc;
...
```
#### deny-tor_ips.conf
"deny" list of IP addresses separated by semicolons.
##### Example
```
deny 101.99.84.87;
deny 101.99.84.87;
deny 2001:1620:51a1:0:8aae:ddff:fe61:8ccc;
...
```

#### set_real_ip_from-tor_ips.conf
"set_real_ip_from" list of IP addresses separated by semicolons.
##### Example
```
set_real_ip_from 101.99.84.87;
set_real_ip_from 101.99.84.87;
set_real_ip_from 2001:1620:51a1:0:8aae:ddff:fe61:8ccc;
...
```
