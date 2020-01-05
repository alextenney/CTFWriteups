# The Vault

CTF: PicoCTF 2018. 
Category: Web Exploitation
Points: 250
Description: There is a website running at http://2018shell.picoctf.com:49030 (link [1] ). 
Try to see if you can login!
Hint(s): None
Author: Alexandra Tenney

## Solution

There is PHP source code available at the bottom of this page, and in that source code the query uses string concatentation
which makes the databse vulnerable to SQL injection, so it was the first thing I tried. It gave me an error that said 
"SQLi" detected. Upon further inspection of the code you can see that this validation code is only hooked up to the 
username, but not the password. Thus only put the SQL Injection in the password field. 

Username: <blank>
Password: ' OR '1'='1' --

## The Full Flag

ppicoCTF{w3lc0m3_t0_th3_vau1t_c4738171}