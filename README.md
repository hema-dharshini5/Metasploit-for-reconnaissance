## Name : Hema Dharshini N
## reg no: 212223220034
# Metasploit-for-reconnaissance
# Metasploit
Metasploit for reconnaissance in pentesting

# AIM:

To get introduced to Metasploit Framework and to  perform reconnaissance  in pentesting .

## DESIGN STEPS:

### Step 1:

Install kali linux either in partition or virtual box or in live mode

### Step 2:

Investigate on the various categories of tools as follows:

### Step 3:

Open terminal and try execute some kali linux commands

## EXECUTION STEPS AND ITS OUTPUT:


## OUTPUT:
![ethi 1](https://github.com/hema-dharshini5/Metasploit-for-reconnaissance/assets/147117728/35242a16-99ef-4ed7-bcca-c3d9160fdc07)

Invoke msfconsole

## OUTPUT:
![eth2](https://github.com/hema-dharshini5/Metasploit-for-reconnaissance/assets/147117728/c3c21cc8-2a1e-49b6-a3c0-5901f9135fdd)

Type help or a question mark "?" to see the list of all available commands you can use inside msfconsole.
## OUTPUT:
![ep 5 3 eth](https://github.com/hema-dharshini5/Metasploit-for-reconnaissance/assets/147117728/6217623e-7ee2-419b-989c-f21948cfc7cc)

Port Scanning: Following command is executed for scanning the systems on our local area network with a TCP scan (-sT) looking for open ports between 1 and 1000 (-p1-1000). msf > nmap -sT 192.168.1810/24 -p1-1000
## OUTPUT:
![ethep 5 4](https://github.com/hema-dharshini5/Metasploit-for-reconnaissance/assets/147117728/7026f5a5-e0c4-4334-b21b-ff787e6ed08c)

use the db-nmap command to scan and save the results into Metasploit's postgresql attached database. In that way, you can use those results in the exploitation stage later.

scan the targets with the command db_nmap as follows. msf > db_nmap 192.168.181.0/24

## OUTPUT:
![eth ep 5 5](https://github.com/hema-dharshini5/Metasploit-for-reconnaissance/assets/147117728/8fe995a9-5207-44c2-bf8c-791a747c73b1)

Metasploit has a multitude of scanning modules built in. If we open another terminal, we can navigate to Metasploit's auxiliary modules and list all the scanner modules. cd /usr/share /metasploit-framework/modules/auxiliary kali > ls -l

## OUTPUT:
![ETHEP 5 6](https://github.com/hema-dharshini5/Metasploit-for-reconnaissance/assets/147117728/67118d96-b85c-475c-a504-ccea2017f716)

Search is a powerful command in Metasploit that you can use to find what you want to locate. msf >search name:Microsoft type:exploit

## OUTPUT:
![ETHEP 5 7](https://github.com/hema-dharshini5/Metasploit-for-reconnaissance/assets/147117728/b1573cce-349d-47f1-a313-646c04c9e457)

The info command provides information regarding a module or platform.
## OUTPUT:
![ETH EP 5 8](https://github.com/hema-dharshini5/Metasploit-for-reconnaissance/assets/147117728/5549ab1c-587e-4f96-ba74-4d50453277f7)


Before beginning, set up the Metasploit database by starting the PostgreSQL server and initialize msfconsole database as follows: systemctl start postgresql msfdb init ##MYSQL ENUMERATION Find the IP address of the Metasploitable machine first. Then, use the db_nmap command in msfconsole with Nmap flags to scan the MySQL database at 3306 port. db_nmap -sV -sC -p 3306 <metasploitable_ip_address>

## OUTPUT:
![ETH EP 5 10](https://github.com/hema-dharshini5/Metasploit-for-reconnaissance/assets/147117728/16704fbc-6c87-4a91-8b92-4329e5c55d26)

Use the search option to look for an auxiliary module to scan and enumerate the MySQL database. search type:auxiliary mysql

## OUTPUT:
![ETH EP 5 11](https://github.com/hema-dharshini5/Metasploit-for-reconnaissance/assets/147117728/27acfcbd-1281-46ab-abf6-4e0ffba5df42)

use 11 Or: use auxiliary/scanner/mysql/mysql_version
## OUTPUT:
![eth ep 5 12](https://github.com/hema-dharshini5/Metasploit-for-reconnaissance/assets/147117728/d1802e05-9a5b-498c-9d5a-8fe33b11a617)

Use the set rhosts command to set the parameter and run the module, as follows:
## OUTPUT:
![eth ep 5 13](https://github.com/hema-dharshini5/Metasploit-for-reconnaissance/assets/147117728/5d2edb0c-daea-462f-bd8a-edb7b7513b95)

After scanning, you can also brute force MySQL root account via Metasploit's auxiliary(scanner/mysql/mysql_login) module.
## OUTPUT:
![eth ep5 14](https://github.com/hema-dharshini5/Metasploit-for-reconnaissance/assets/147117728/a858af09-5ef4-46fb-b76f-f694e891145c)

set the PASS_FILE parameter to the wordlist path available inside /usr/share/wordlists: set PASS_FILE /usr/share/wordlistss/rockyou.txt Then, specify the IP address of the target machine with the RHOSTS command. set RHOSTS Set BLANK_PASSWORDS to true in case there is no password set for the root account. set BLANK_PASSWORDS true
## OUTPUT:
![ETH EP 5 15](https://github.com/hema-dharshini5/Metasploit-for-reconnaissance/assets/147117728/0fcff5f1-309c-466f-ae47-6db1e70f8b59)


## RESULT:
The Metasploit framework for reconnaissance is  examined successfully
