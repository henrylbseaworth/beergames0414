beergames0414
=============
Obfuscation Part One (I) 
Week(s) of (and after) July 17, 2014 beer games (numero 4!).

Part I Due: Thursday, July 24 at Midnight MST.

Challenge
-----
This challenge consists of two parts. In the first, each participant will develop two programs. The first program will encrypt/obfuscate a text tile. It will take a key (maximum of 256 bits) and a file path.  The file will be encrypted with the given key.  The second program will take a key and an encrypted file (perhaps referred to as a cyphertext) and decrypt it (to the original plain-text). 

The second part of this challenge involves cracking other participants' encryptions. Keep that in mind but don't worry about it for now. It should be noted that no encryption libraries are allowed (e.g. if you can't explain how something works in simple logic you can't use it).


Example
-----
Let's take a simple cypher example. This is so simple that it only works for ASCII encoded text; it maps each ASCII character to KEY number of characters after it (with rollover). 

Given the following plain text:

			Non eram nescius, Brute, cum, quae summis ingeniis exquisitaque doctrina philosophi Graeco sermone tractavissent, ea Latinis litteris mandaremus, fore ut hic noster labor in varias reprehensiones incurreret. 

The cypher generates the following "cypher text" when the key is "1":

		Opo!fsbn!oftdjvt-!Csvuf-!dvn-!rvbf!tvnnjt!johfojjt!fyrvjtjubrvf!epdusjob!qijmptpqij!Hsbfdp!tfsnpof!usbdubwjttfou-!fb!Mbujojt!mjuufsjt!nboebsfnvt-!gpsf!vu!ijd!optufs!mbcps!jo!wbsjbt!sfqsfifotjpoft!jodvssfsfu/!

Notice that each character in the cypher text is exactly the ASCII character after the same character in the plain text. E.g. "Non " maps to "Opo!" (look at an ASCII table to check!). 
It turns out this scheme is actually some bastardized version of a Caesar cypher and if we make a decryption program we will get the original text back! 

			Non eram nescius, Brute, cum, quae summis ingeniis exquisitaque doctrina philosophi Graeco sermone tractavissent, ea Latinis litteris mandaremus, fore ut hic noster labor in varias reprehensiones incurreret. 

## General Beer Games Rules (still preliminary)

You can use any languages/libraries/hax so long as it works on the test machine (talk to the l33t team for which are installed/adding more). Whoever completes the program is invited to a venue to drink beer. Whoever "wins" the challenge chooses the venue and gets a secret surpise gift, decided upon by the l33t team. 

This is a special Beer Games because winners will get a beer purchased by the l33t team. If you're under 21 then you'll still get a beer, but you may not be able to drink it.

### Programs
Contestants can enter any number of programs. Programs can use any language but are asked to not use a real encryption library/plugin/framework/etc...

### Submissions
Make a folder in the root directory of the repository. The name of this folder is your handle, you can choose anything except "dasboot" (that's where we'll keep all the tests and benchmarking stuff). Put all your submissions in your folder. If you submit more than one program you'll also need a file called "programlist" that contains a list of all your submissions. Here's an example programlist file:

        ./mysubmittion.py  #for a script that has #!/usr/local/bin/python
        ruby myothersubmission.rb    #for a script that doesn't have #!/usr/local/bin/ruby
        ./mycprogram.out    #a compiled program

For those not fammiliar with Git, if I wanted to submit my program called SortingIPAs.sh I could use the following procedure:

```bash
git clone https://github.com/henrylbseaworth/beergames0214.git
cd beergames0214

#create my folder/handle and copy in my submission
mkdir -p baconsSubs && cp SortingIPAs.sh baconsSubs/

git add baconsSubs/SortingIPAs.sh #add my submission to be tracked 
git commit -m "added my submission yay!"    #commit this change to the stage
git push -u orign master    #push my changes to the repo
```

Another Git-tip: *it's a good idea to always pull before making changes and before pushing changes. For example if you run ```bash git pull``` before editing/commiting you'll save a bit of headeach if your changes affect other people's changes.  This shouldn't be an issue here but since we're all trying to learn ;D*


About
-----
The Beer Games are a friendly challenge meant to ~~celebreate drinking~~ keep programmers' minds sharp. They're also a good oportunity to teach yourself something new and look at other developer's solutions. 


