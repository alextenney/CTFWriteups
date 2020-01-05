# Secret Agent

CTF: PicoCTF 2018. 
Category: Web Exploitation
Points: 200
Description: Here's a little website that hasn't fully been finished. 
But I heard google gets all your info anyway. http://2018shell.picoctf.com:3827 (link [1] )
Hint(s): (1) How can your browser pretend to be something else?
Author: Alexandra Tenney

## Solution

The challenge asks me how my browser can pretend to be someone else, and when I try and access the flag it
tells me that I'm not google, so somehow I have to pretend to be google. This website shows you different
google user agents: https://support.google.com/webmasters/answer/1061943?hl=en. I used "Mozilla/5.0 
(Linux; Android 6.0.1; Nexus 5X Build/MMB29P) AppleWebKit/537.36 (KHTML, like Gecko) 
Chrome/W.X.Y.Z‡ Mobile Safari/537.36 (compatible; Googlebot/2.1; +http://www.google.com/bot.html)", and then 
switched over the shell. We can use the command curl to specify a user agent. 

This is the command: curl --user-agent "Mozilla/5.0 (Linux; Android 6.0.1; Nexus 5X Build/MMB29P) 
AppleWebKit/537.36 (KHTML, like Gecko) Chrome/W.X.Y.Z‡ Mobile Safari/537.36 
(compatible; Googlebot/2.1; +http://www.google.com/bot.html)""http://2018shell.picoctf.com:3827/flag"

Suddenly the website thinks we are google and we are given the flag.

## The Full Flag

picoCTF{s3cr3t_ag3nt_m4n_12387c22}