# Logon

CTF: PicoCTF 2018. 
Category: Web Exploitation
Points: 150
Description: I made a website so now you can log on to! I don't seem to have the admin password. 
See if you can't get to the flag. http://2018shell.picoctf.com:37861 (link [1] )
Hint(s): (1) Hmm it doesn't seem to check anyone's password, except for admins? 
(2) How does check the admin's password?
Author: Alexandra Tenney

## Solution

When you try to log in to this webpage using any combination of username and password, it allows the user on, but it 
seems only admins can see the flag. I installed a google chrome extension called "Edit This Cookie" in order to see 
the cookies that the website stores. 

Heres a link: https://chrome.google.com/webstore/detail/editthiscookie/fngmhnnpilhplaeedifhccceomclgfbg?hl=en

The website stores three cookies, one for username, one for password, and one for admin. The admin cookie currently
says false, but using my application I can change it to say True, and reload the page!

## The Full Flag

picoCTF{l0g1ns_ar3nt_r34l_a280e12c}