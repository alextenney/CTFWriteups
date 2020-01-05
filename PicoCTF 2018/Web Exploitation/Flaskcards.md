# Flaskcards

CTF: PicoCTF 2018. 
Category: Web Exploitation
Points: 350
Description: We found this fishy website [1]  for flashcards that we think may be sending secrets. 
Could you take a look?
Hint(s): (1) Are there any common vulnerabilities with the backend of the website? (2) Is there 
anywhere that filtering doesn't get applied? (3) The database gets reverted every 2 hours so your 
session might end unexpectedly. Just make another user.
Author: Alexandra Tenney

## Solution

Since flask (a web framework within python) is know for being paticularily vulnerable to a template injection, 
and the name of the challenge refers to flask, we know that this challenge is asking for that type of injection. As
well, we need to find somewhere where the input isn't filtered, so the login page and register page are no longer options.
Once you make an account you are able to make your own flashcards, and the input in these probably isnt filtered. if you
write {{ config }} in one of the cards, it displays the flag.

## The Full Flag

picoCTF{secret_keys_to_the_kingdom_584f8327}