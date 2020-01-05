# Inspect Me

CTF: PicoCTF 2018. 
Category: Web Exploitation
Points: 125
Description: Inpect this code! http://2018shell.picoctf.com:47428 (link [1] )
Hint(s): (1) How do you inspect a website's code on a browser? (2) Check all the website code.
Author: Alexandra Tenney

## First Flag

The challenge is called Inpect Me, so the first thing I tried to do was inpect the page, 
there I found a comment within the HTML with the first 1/3 of the flag: picoCTF{ur_4_real_inspe

### Second Flag

In the about section of the website, the author of the page says they have been practicing HTML, CSS 
and JS, since the first flag was found in the HTML, maybe the next flag will be in the CSS.
When you click inspect there is a link to the css of the webpage. I went to http://2018shell.picoctf.com:47428/mycss.css
of the page and in a comment found the second part of the flag: ct0r_g4dget_e96dd105}

### Third Flag

Since my intuition about the three parts worked, maybe now I should see if I can make it to the JS
for this webpage. Following the same steps I travelled to http://2018shell.picoctf.com:47428/myjs.js, 
in which the flag was empty... meaning I guess I had already found the full flag.


## The Full Flag

picoCTF{ur_4_real_inspect0r_g4dget_e96dd105}

