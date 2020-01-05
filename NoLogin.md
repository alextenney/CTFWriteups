# No Login

CTF: PicoCTF 2018. 
Category: Web Exploitation
Points: 200
Description: Looks like someone started making a website but never got around to making a login, 
but I heard there was a flag if you were the admin. http://2018shell.picoctf.com:14664 (link [1] )
Hint(s): (1) What is it actually looking for in the cookie?
Author: Alexandra Tenney

## Solution

When I try to login, the website tells me this part hasn't been implemented yet, so the page is unfinished.
I decided to inspect the code and found that the page http://2018shell.picoctf.com:14664/flag exists, but 
when I try to go there it tells me I am not an admin. I remember I was able to change a cookie in a previous challenge 
to become an admin, so again I look at the cookies this page stores... there are none. "Edit this Cookie" also 
allows me to make cookies, so I make one called admin and make the value = True. Now when I go to 
http://2018shell.picoctf.com:14664/flag, it lets me!

## The Full Flag

picoCTF{n0l0g0n_n0_pr0bl3m_eb9bab29}