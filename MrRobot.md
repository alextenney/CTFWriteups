# Mr.Robot

CTF: PicoCTF 2018. 
Category: Web Exploitation
Points: 200
Description: Do you see the same things I see? The glimpses of the flag hidden away? 
http://2018shell.picoctf.com:10157 (link [1] )
Hint(s): (1) What part of the website could tell you where the creator doesn't want you to look?
Author: Alexandra Tenney

## Solution

The webpage for this one is pretty bare, so I decided to inspect the code. In the HTML you can see that the 
author of the page had hidden something, but it is unclear exactly what. Maybe if we just look at the text of the
website rather than the HTML we will be able to see something? I go to http://2018shell.picoctf.com:10157/robots.txt
but am given a disallowed message.

Paired with this message I am sent to an html page... http://2018shell.picoctf.com:10157/143ce.html

When I go to that page the flag is revealed! 

## The Full Flag

picoCTF{th3_w0rld_1s_4_danger0us_pl4c3_3lli0t_143ce}