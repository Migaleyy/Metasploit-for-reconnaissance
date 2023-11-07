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

## PROGRAM:
Find out the ip address of the attackers system## OUTPUT:

![image](https://github.com/Migaleyy/Metasploit-for-reconnaissance/assets/118262199/a486979e-c0e6-4c9a-ab6a-4832cb1d9007)

## invoke msfconsole:

![image](https://github.com/Migaleyy/Metasploit-for-reconnaissance/assets/118262199/0beba95a-69b0-40ed-aa91-e57828ddf8c5)

Type help or a question mark "?" to see the list of all available commands you can use inside msfconsole.

## OUTPUT:

![image](https://github.com/Migaleyy/Metasploit-for-reconnaissance/assets/118262199/13d88209-f7b7-45bc-9190-dae3ad680cce)

Port Scanning: Following command is executed for scanning the systems on our local area network with a TCP scan (-sT) looking for open ports between 1 and 1000 (-p1-1000). msf > nmap -sT 192.168.1810/24 -p1-1000

![image](https://github.com/Migaleyy/Metasploit-for-reconnaissance/assets/118262199/b91d86f6-0dde-4d2d-8f4d-87ef9fa7e28b)

Metasploit has a multitude of scanning modules built in. If we open another terminal, we can navigate to Metasploit's auxiliary modules and list all the scanner modules. cd /usr/share /metasploit-framework/modules/auxiliary kali > ls -l

![image](https://github.com/Migaleyy/Metasploit-for-reconnaissance/assets/118262199/141c3c1a-eee6-4282-86fe-5332b486db57)
![image](https://github.com/Migaleyy/Metasploit-for-reconnaissance/assets/118262199/7bdafa63-9ab6-456f-a672-f2dda44b5879)

Search is a powerful command in Metasploit that you can use to find what you want to locate. msf >search name:Microsoft type:exploit.
![image](https://github.com/Migaleyy/Metasploit-for-reconnaissance/assets/118262199/6c9ead05-d5a0-4ade-91bf-0075e435431b)
The info command provides information regarding a module or platform.

![image](https://github.com/Migaleyy/Metasploit-for-reconnaissance/assets/118262199/4c62b628-1ca3-4be0-8703-2372d029a25d)

Before beginning, set up the Metasploit database by starting the PostgreSQL server and initialize msfconsole database as follows: systemctl start postgresql msfdb init ##MYSQL ENUMERATION Find the IP address of the Metasploitable machine first. Then, use the db_nmap command in msfconsole with Nmap flags to scan the MySQL database at 3306 port. db_nmap -sV -sC -p 3306 <metasploitable_ip_address>.
![image](https://github.com/Migaleyy/Metasploit-for-reconnaissance/assets/118262199/38e81df9-d135-40ba-8413-2c96a022c383)
Use the search option to look for an auxiliary module to scan and enumerate the MySQL database. search type:auxiliary mysql.
![image](https://github.com/Migaleyy/Metasploit-for-reconnaissance/assets/118262199/62a1267f-d001-4c42-8199-3bc20328529a)
Use the auxiliary/scanner/mysql/mysql_version module by typing the module name or associated number to scan MySQL version details. use 11 Or: use auxiliary/scanner/mysql/mysql_version.
![image](https://github.com/Migaleyy/Metasploit-for-reconnaissance/assets/118262199/3ca5cded-1dbc-4115-86a3-b31cd43568e0)
After scanning, you can also brute force MySQL root account via Metasploit's auxiliary(scanner/mysql/mysql_login) module.
![image](https://github.com/Migaleyy/Metasploit-for-reconnaissance/assets/118262199/d5b7a3ac-59e7-440c-8008-a7e7ff506f8b)
set the PASS_FILE parameter to the wordlist path available inside /usr/share/wordlists: set PASS_FILE /usr/share/wordlistss/rockyou.txt Then, specify the IP address of the target machine with the RHOSTS command. set RHOSTS Set BLANK_PASSWORDS to true in case there is no password set for the root account. set BLANK_PASSWORDS true.
![image](https://github.com/Migaleyy/Metasploit-for-reconnaissance/assets/118262199/3334a849-debb-43ae-815d-22df9f026104)

## RESULT:
The Metasploit framework for reconnaissance is  examined successfully
