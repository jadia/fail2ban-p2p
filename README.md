# fail2ban-p2p

This is the repository for fail2ban-p2p. Fail2ban-p2p is a standalone
application written in python that will exchange IPs of attackers detected
by [fail2ban](http://www.fail2ban.org) using a p2p-network.

## Basic concept

- Every node in the p2p-network is connected to at least one other 'friend'
- friends exchange their public keys to verify messages signed with the senders private key.
- Nodes send each other messages when one of them detected an attacker
- Nodes also pass along this information to spread it in the network
- You can assign different trustlevels for friends and a threshold that is required to ban an attacker locally.

## Documentation

See [http://fail2ban-p2p.comuno.net](http://fail2ban-p2p.comuno.net) or the folder `doc/` for documentation about installation and configuration

## Directory structure

> config            sample configuration  
> debian            necessary files for creating packages for debian  
> doc/              home of all documentation  
> fail2ban-p2p/     classes and functions  
> scripts/          scripts for building fail2ban-p2p releases  
> tests/            testcases, if any  

## Short coding styleguide

- One class per file
- One directory per package
- One tab = 4 spaces
- lower-case variables, if it consists of multiple words, beginning of every new word is upper-case, e.g.: donauDampfSchiffFahrtsGesellschaft, protocolVersion, tmp
- the above is also true for function names
- class names behave similarly, except for the fact that they begin with a capital letter.
