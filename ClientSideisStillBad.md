# Client Side is Still Bad

CTF: PicoCTF 2018. 
Category: Web Exploitation
Points: 150
Description: I forgot my password again, but this time there doesn't seem to be a reset, can you help me? 
http://2018shell.picoctf.com:55790 (link [1] )
Hint(s): (1) Client Side really is a bad way to do it.
Author: Alexandra Tenney

## Solution

The challenge title eludes to something being show or coded on the client side that shouldn't be, so I decided to
inspect the page. Upon inspection you find this following function:


  function verify() {
    checkpass = document.getElementById("pass").value;
    split = 4;
    if (checkpass.substring(split*7, split*8) == '}') {
      if (checkpass.substring(split*6, split*7) == 'd366') {
        if (checkpass.substring(split*5, split*6) == 'd_3b') {
         if (checkpass.substring(split*4, split*5) == 's_ba') {
          if (checkpass.substring(split*3, split*4) == 'nt_i') {
            if (checkpass.substring(split*2, split*3) == 'clie') {
              if (checkpass.substring(split, split*2) == 'CTF{') {
                if (checkpass.substring(0,split) == 'pico') {
                  alert("You got the flag!")
                  }
                }
              }
      
            }
          }
        }
      }
    }
    else {
      alert("Incorrect password");
    }
  }
  
  If you put this all together, you've got the flag!


## The Full Flag

picoCTF{client_is_bad_3bd366}
