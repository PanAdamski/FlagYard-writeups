# Patchi

nmap scan
```
22/tcp   open  ssh     OpenSSH 8.9p1 Ubuntu 3 (Ubuntu Linux; protocol 2.0)
| ssh-hostkey: 
|   256 ae:4b:e7:a3:bc:f3:59:79:e7:49:b4:39:1e:76:e7:27 (ECDSA)
|_  256 a9:a7:82:2f:76:85:53:66:56:55:a4:fa:36:6a:04:84 (ED25519)
8081/tcp open  http    Apache httpd 2.4.50 ((Unix))
|_http-server-header: Apache/2.4.50 (Unix)
| http-methods: 
|   Supported Methods: OPTIONS HEAD GET POST TRACE
|_  Potentially risky methods: TRACE
|_http-title: Site doesn't have a title (text/html).
```

Apache/2.4.50 (Unix) is interesting

I tried https://www.exploit-db.com/exploits/50446

![{59803E64-59D0-4736-B8F1-B0FC8AA18179}](https://github.com/user-attachments/assets/53c126a0-ae84-4f9a-b280-5f9140556592)

Fast RCE

![{90594BE9-D404-4613-8898-039BADD7F2C8}](https://github.com/user-attachments/assets/5d1d7dd5-4fdc-4719-a939-77eb975f213c)


jakbym chciał coś wrzucić na maszynkę to lekkie problemy

![{5F935011-5720-4AD5-82F1-37D9057EEEA9}](https://github.com/user-attachments/assets/6be8c8c0-a20d-41f0-9616-a42a51656fcd)

So we are on the docker
![{30FA573B-B0AE-486E-87DA-D54B0541C611}](https://github.com/user-attachments/assets/9b7d3317-395c-4c87-b72d-dc9ed558c702)


to ciekawe `/usr/local/apache2/bin/suexec`

