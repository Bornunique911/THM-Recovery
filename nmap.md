```console
# Nmap 7.91 scan initiated Sat Oct 16 09:01:08 2021 as: nmap -vvv -p 22,80,1337,65499 -A -oN nmap 10.10.234.25
Nmap scan report for 10.10.234.25 (10.10.234.25)
Host is up, received syn-ack (0.21s latency).
Scanned at 2021-10-16 09:02:19 IST for 73s

PORT      STATE SERVICE REASON  VERSION
22/tcp    open  ssh     syn-ack OpenSSH 7.9p1 Debian 10+deb10u2 (protocol 2.0)
| ssh-hostkey: 
|   2048 55:17:c1:d4:97:ba:8d:82:b9:60:81:39:e4:aa:1e:e8 (RSA)
| ssh-rsa AAAAB3NzaC1yc2EAAAADAQABAAABAQCqaXDoAAvwHBvNhrHfjZaxCgLbQAImpPRiPxxetRqPQYVPusw2lV6HPV1j2ymgdsaA7bNP8jroSq54c2mVLyYVYwbdUscYuLMj/RflPxHx/18J2LF0FnhyRsX8iszNqQ+BqDQ74O2hyN/Cqbwy8pm6i75QRIBlyFRzFwihqSqCDp9OO75Y9wr2+iQX8yzL7CJjnS5w+vEdnGsf88Mzs/NZxB2ZHoDf3lw8uMo0iHg23GfPntVilr01AP6szDOHIMlMMk6pMqkU7MrXvJz+Ij+MP8b1+5T0uBB4MgtrUyQLXyRZGX4M30YGdR+jnfAjIKEjAEqrSyotr+l+hLEgUNHT
|   256 8d:f5:4b:ab:23:ed:a3:c0:e9:ca:90:e9:80:be:14:44 (ECDSA)
| ecdsa-sha2-nistp256 AAAAE2VjZHNhLXNoYTItbmlzdHAyNTYAAAAIbmlzdHAyNTYAAABBBCjzHLHSekU/G6uRjXbHIsERaRTzJ+a1lVwvIXkLoaqhlHIM616JxWkaUD0CxzLjrnSjxKsjI1YXcrHYFNd2rys=
|   256 3e:ae:91:86:81:12:04:e4:70:90:b1:40:ef:b7:f1:b6 (ED25519)
|_ssh-ed25519 AAAAC3NzaC1lZDI1NTE5AAAAIHR259lx5M/24wvX1dnbS1ehHzmK4sr1B7aZqsfIesOB
80/tcp    open  http    syn-ack Apache httpd 2.4.43 ((Unix))
| http-methods: 
|   Supported Methods: OPTIONS HEAD GET POST TRACE
|_  Potentially risky methods: TRACE
|_http-server-header: Apache/2.4.43 (Unix)
|_http-title: Site doesn't have a title (text/html).
1337/tcp  open  http    syn-ack nginx 1.14.0 (Ubuntu)
| http-methods: 
|_  Supported Methods: HEAD GET OPTIONS
|_http-server-header: nginx/1.14.0 (Ubuntu)
|_http-title: Help Alex!
65499/tcp open  ssh     syn-ack OpenSSH 7.6p1 Ubuntu 4ubuntu0.3 (Ubuntu Linux; protocol 2.0)
| ssh-hostkey: 
|   2048 b9:b6:aa:93:8d:aa:b7:f3:af:71:9d:7f:c5:83:1d:63 (RSA)
| ssh-rsa AAAAB3NzaC1yc2EAAAADAQABAAABAQDIefQd78mUpATjIg691Z6jdxWq6XjvivNMdaV3PrE70ee0YPwQxQwNYswl7v1k+r9c1PENL8ol4wokp/nk2omQP3Iwua/STVYo6Xdh9DIgC7x68FWaJn/t24zhKKZ/v8vHIIulI5sdHTQzapVgIqhZFHW1JhvmdObuKGccGRQddPElr2pwguwSdNOzW21h8LPMr7wEiafbaLhM09fEN0UUWwDF4RfFo5GoW7Mhz4Y64PxlH6CbrAS/z0sPe7F3nx2/YNdvM83VNNtGCSOnSbmt0AbgZHh/Zv05RM8p1QR4EoMSi4ogQW6VH78GNRROG2V+P56u1VQ/Je6CXLMWML69
|   256 64:98:14:38:ff:38:05:7e:25:ae:5d:33:2d:b6:78:f3 (ECDSA)
| ecdsa-sha2-nistp256 AAAAE2VjZHNhLXNoYTItbmlzdHAyNTYAAAAIbmlzdHAyNTYAAABBBEFh4xjNznqUWlomutlVT1AIG/RmduH5bjmze2euH63jQRqYS1h8Y4Negc4cw4CXm3HpkxtYctO4VAaGwHCGNWk=
|   256 ef:2e:60:3a:de:ea:2b:25:7d:26:da:b5:6b:5b:c4:3a (ED25519)
|_ssh-ed25519 AAAAC3NzaC1lZDI1NTE5AAAAIC/31imc1cKaUsvUlgomJ1RGFpLTNcb1YDT+TDXJ03R5
Service Info: OS: Linux; CPE: cpe:/o:linux:linux_kernel

Read data files from: /usr/bin/../share/nmap
Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
# Nmap done at Sat Oct 16 09:03:32 2021 -- 1 IP address (1 host up) scanned in 145.84 seconds
```
