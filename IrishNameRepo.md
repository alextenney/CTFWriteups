# Irish Name Repo

CTF: PicoCTF 2018. 
Category: Web Exploitation
Points: 200
Description: There is a website running at http://2018shell.picoctf.com:59464 (link [1] ). 
Do you think you can log us in? Try to see if you can login!
Hint(s): (1) There doesn't seem to be many ways to interact with this, I wonder if the 
users are kept in a database?
Author: Alexandra Tenney

## Solution

Since the hint says that the repo was connected to a database, I tried the only database vulnerability 
I knew anything about... a SQL Injection. Upon a little research I came across this one: ' OR '1'='1' --
and tried it as the username and password. I got in!

Ill later find out that if you inspect the page, you'll notice the form is called login.php. Php tends to 
be really vulnerable to SQL injection, so if you notice it being used you should probably try a SQL Injection!

## The Full Flag

picoCTF{con4n_r3411y_1snt_1r1sh_d121ca0b}