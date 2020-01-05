# Buttons

CTF: PicoCTF 2018. 
Category: Web Exploitation
Points: 250
Description: There is a website running at http://2018shell.picoctf.com:7949 (link [1] ). 
Try to see if you can push their buttons.
Hint(s): (1) What's different about the two buttons?
Author: Alexandra Tenney

## Solution

Just clicking button 1 sends us to the next page, but the POST method for button 2 is disabled (you can see this in the HTML
comment for the page). We can use the curl command in the terminal in order to specify the method, to ensure it POSTS
to http://2018shell.picoctf.com:7949/button2.php. 

The full command: curl -X POST http://2018shell.picoctf.com:7949/button2.php  

## The Full Flag

picoCTF{button_button_whose_got_the_button_3e5652dd}