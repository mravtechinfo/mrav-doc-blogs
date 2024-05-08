pico_CTF_writeup_2024_by_mravetchinfo

**Challenge Name:** Bookmarklet




**Challenge Description:**

In this challenge, participants are provided with a webpage hosted at [http://titan.picoctf.net:55173/](http://titan.picoctf.net:55173/) and are tasked with finding the flag. However, instead of manually searching for the flag within the webpage, the challenge suggests creating a bookmarklet to automate the process.



**Solution:**

To automate the flag retrieval process, we can use JavaScript to decrypt the encrypted flag provided on the webpage. Below is the JavaScript code used for decryption:

```javascript
javascript:(function() {
    var encryptedFlag = "àÒÆÞ¦È¬ëÙ£ÖÓÚåÛÑ¢ÕÓÔÅÐÙí";
    var key = "picoctf";
    var decryptedFlag = "";
    for (var i = 0; i < encryptedFlag.length; i++) {
        decryptedFlag += String.fromCharCode((encryptedFlag.charCodeAt(i) - key.charCodeAt(i % key.length) + 256) % 256);
    }
    alert(decryptedFlag);
    // Flag: picoCTF{p@g3_turn3r_1d1ba7e0}
})();
```

This JavaScript code decrypts the encrypted flag using a simple XOR cipher with a key of "picoctf". The decrypted flag is `picoCTF{p@g3_turn3r_1d1ba7e0}`.



**How to Use the Bookmarklet:**

1. Create a new bookmark in your web browser.
2. Edit the bookmark's properties and give it a name, such as "Decrypt Flag."
3. Paste the JavaScript code provided above into the URL or Address field of the bookmark. Ensure that the code is preceded by `javascript:` to indicate that it is JavaScript code.
4. Save the bookmark.
5. Navigate to the provided webpage ([http://titan.picoctf.net:55173/](http://titan.picoctf.net:55173/)).
6. Click on the bookmarklet created in step 2.
7. An alert will pop up displaying the decrypted flag: `picoCTF{p@g3_turn3r_1d1ba7e0}`.



**Conclusion:**

Using a simple XOR cipher and a bookmarklet, we were able to automate the decryption of the flag provided on the webpage, making the flag retrieval process more efficient. Bookmarklets can be powerful tools in CTFs for automating tasks and solving challenges more quickly.



**References:**

- [PicoCTF](http://titan.picoctf.net:55173/)
- [CTF Writeup Guidelines](https://undraw.co/)

---




--------------------------------------------------------------------------------------------------------------------------

**CTF Writeup: Decoding Flags using Web Inspector**



**Challenge Name:** WebDecode  
**Author:** Nana Ama Atombo-Sackey

**Description:**  
In the "WebDecode" challenge, participants are instructed to use the web inspector to find the flag. The challenge provides a webpage hosted at [http://titan.picoctf.net:57534/](http://titan.picoctf.net:57534/). Upon inspecting the webpage, participants discover a section with an attribute `notify_true` containing encoded text: `<section class="about" notify_true="cGljb0NURnt3ZWJfc3VjYzNzc2Z1bGx5X2QzYzBkZWRfZGYwZGE3Mjd9">`. The challenge hints at using tools like CyberChef to decode the flag.

**Decoded Flag:**  

picoCTF{web_succ3ssfully_d3c0ded_df0da727}



**Conclusion:**  
By inspecting the webpage and decoding the encoded text found in the HTML using CyberChef or similar tools, participants were able to successfully retrieve the flag. This challenge demonstrates the importance of understanding web technologies and utilizing web inspector tools in CTFs.



**References:**  

- [PicoCTF - WebDecode Challenge](http://titan.picoctf.net:57534/)
- [CyberChef](https://gchq.github.io/CyberChef/)




--------------------------------------------------------------------------------------------------------------------------


Challenge name - Unminify



AUTHOR: JEFFERY JOHN

Description
I don't like scrolling down to read the code of my website, so I've squished it. As a bonus, my pages load faster!
Browse here, and find the flag!

http://titan.picoctf.net:51196/

 curl http://titan.picoctf.net:51196/ | grep -o 'picoCTF{[^}]*}' 
 
 
 picoCTF{pr3tty_c0d3_622b2c88}
 
 ---
 
 --------------------------------------------------------------------------------------------------------------------------
 
 Challenge name :IntroToBurp
 
 http://titan.picoctf.net:54461/
 
 
  picoCTF{#0TP_Bypvss_SuCc3$S_2e80f1fd}

just intercept the form you get the /dashboard redirection

then it will give the otp parametr jsut play with it
I removed it lol got the flag

---

 --------------------------------------------------------------------------------------------------------------------------
 
 
 Chall name - Super SSH
AUTHOR: JEFFERY JOHN

Description
Using a Secure Shell (SSH) is going to be pretty important.
Can you ssh as ctf-player to titan.picoctf.net at port 49566 to get the flag?
You'll also need the password 1db87a14. If asked, accept the fingerprint with yes.
If your device doesn't have a shell, you can use: https://webshell.picoctf.org
If you're not sure what a shell is, check out our Primer: https://primer.picoctf.com/#_the_shell

```
ssh  ctf-player@titan.picoctf.net -p  49566
The authenticity of host '[titan.picoctf.net]:49566 ([3.139.174.234]:49566)' can't be established.
ED25519 key fingerprint is SHA256:4S9EbTSSRZm32I+cdM5TyzthpQryv5kudRP9PIKT7XQ.
This key is not known by any other names.
Are you sure you want to continue connecting (yes/no/[fingerprint])? yes
Warning: Permanently added '[titan.picoctf.net]:49566' (ED25519) to the list of known hosts.
ctf-player@titan.picoctf.net's password: 
Welcome ctf-player, here's your flag: picoCTF{s3cur3_c0nn3ct10n_45a48857}
Connection to titan.picoctf.net closed.
```
---

----------------------------------------------------------------------------------------------------------------------------

Commitment Issues
 |  | 50 points
Tags: 
AUTHOR: JEFFERY JOHN

Description
I accidentally wrote the flag down. Good thing I deleted it!
You download the challenge files here:
challenge.zip


https://artifacts.picoctf.net/c_titan/138/challenge.zip

picoCTF{s@n1t1z3_c785c319}


```
!  ~/p/g/drop-in   ~  git checkout b562f0b425907789d11d2fe2793e67592dc6be93
Note: switching to 'b562f0b425907789d11d2fe2793e67592dc6be93'.

You are in 'detached HEAD' state. You can look around, make experimental
changes and commit them, and you can discard any commits you make in this
state without impacting any branches by switching back to a branch.

If you want to create a new branch to retain commits you create, you may
do so (now or later) by using -c with the switch command. Example:

  git switch -c <new-branch-name>

Or undo this operation with:

  git switch -

Turn off this advice by setting config variable advice.detachedHead to false

HEAD is now at b562f0b create flag
 ~/p/g/drop-in  ➦ b562f0b  ls                         Sun Mar 24 02:05:06 2024
message.txt
 ~/p/g/drop-in  ➦ b562f0b  cat message.txt            Sun Mar 24 02:05:16 2024
picoCTF{s@n1t1z3_c785c319}
 ~/p/g/drop-in  ➦ b562f0b   
```

 
 
 ---
 
 
 ----------------------------------------------------------------------------------------------------------------------------
 
 
 
 ime Machine
 |  | 50 points
Tags: 
AUTHOR: JEFFERY JOHN

Description
What was I last working on? I remember writing a note to help me remember...
You can download the challenge files here:
challenge.zip


https://artifacts.picoctf.net/c_titan/162/challenge.zip


git log                      Sun Mar 24 02:10:51 2024
commit 712314f105348e295f8cadd7d7dc4e9fa871e9a2 (HEAD -> master)
Author: picoCTF <ops@picoctf.com>
Date:   Tue Mar 12 00:07:26 2024 +0000

    picoCTF{t1m3m@ch1n3_e8c98b3a}
    
    
---    
    

---------------------------------------------------------------------------------------------------------------------------



Blame Game
 |  | 75 points
Tags: 
AUTHOR: JEFFERY JOHN

Description
Someone's commits seems to be preventing the program from working. Who is it?
You can download the challenge files here:
challenge.zip

git blame message.py                                                                                                                          Sun Mar 24 02:25:28 2024
8c83358c (picoCTF{@sk_th3_1nt3rn_2c6bf174} 2024-03-12 00:07:11 +0000 1) print("Hello, World!"

---

----------------------------------------------------------------------------------------------------------------------------------
Collaborative Development
 |  | 75 points
Tags: 
AUTHOR: JEFFERY JOHN

Description
My team has been working very hard on new features for our flag printing program! I wonder how they'll work together?
You can download the challenge files here:
challenge.zip

```
 ~/p/g/c/d/.git  ls                                                                                                                                                                                                 Sun Mar 24 02:29:48 2024
COMMIT_EDITMSG  HEAD  branches/  config  description  hooks/  index  info/  logs/  objects/  refs/
 ~/p/g/c/d/.git  cd ..                                                                                                                                                                                              Sun Mar 24 02:29:49 2024
 ~/p/g/c/drop-in  ➦ 2258a0f  ls                                                                                                                                                                                    Sun Mar 24 02:29:55 2024
flag.py
 ~/p/g/c/drop-in  ➦ 2258a0f  cat flag.py                                                                                                                                                                           Sun Mar 24 02:29:56 2024
print("Printing the flag...")
 ~/p/g/c/drop-in  ➦ 2258a0f  git log                                                                                                                                                                               Sun Mar 24 02:29:58 2024
commit 2258a0f267d57e8b6025e2a020b77fac7a553c92 (HEAD, main)
Author: picoCTF <ops@picoctf.com>
Date:   Tue Mar 12 00:07:54 2024 +0000

    init flag printer
 ~/p/g/c/drop-in  ➦ 2258a0f  git blame flag.py                                                                                                                                                                     Sun Mar 24 02:30:06 2024
^2258a0f (picoCTF 2024-03-12 00:07:54 +0000 1) print("Printing the flag...")
 ~/p/g/c/drop-in  ➦ 2258a0f  git branch -a                                                                                                                                                                         Sun Mar 24 02:30:14 2024
* (HEAD detached at 2258a0f)
  feature/part-1
  feature/part-2
  feature/part-3
  main
 ~/p/g/c/drop-in  ➦ 2258a0f  git checkout main                                                                                                                                                                     Sun Mar 24 02:30:53 2024
Switched to branch 'main'
 ~/p/g/c/drop-in    ls                                                                                                                                                                                            Sun Mar 24 02:31:07 2024
flag.py
 ~/p/g/c/drop-in    cat flag.py                                                                                                                                                                                   Sun Mar 24 02:31:08 2024
print("Printing the flag...")
 ~/p/g/c/drop-in    git blame flag.py                                                                                                                                                                             Sun Mar 24 02:31:10 2024
^2258a0f (picoCTF 2024-03-12 00:07:54 +0000 1) print("Printing the flag...")
 ~/p/g/c/drop-in    git log                                                                                                                                                                                       Sun Mar 24 02:31:15 2024
commit 2258a0f267d57e8b6025e2a020b77fac7a553c92 (HEAD -> main)
Author: picoCTF <ops@picoctf.com>
Date:   Tue Mar 12 00:07:54 2024 +0000

    init flag printer
 ~/p/g/c/drop-in    git checkout feature/part-1                                                                                                                                                                   Sun Mar 24 02:31:18 2024
Switched to branch 'feature/part-1'
 ~/p/g/c/drop-in   feature/part-1  ls                                                                                                                                                                             Sun Mar 24 02:31:37 2024
flag.py
 ~/p/g/c/drop-in   feature/part-1  cat flag.py                                                                                                                                                                    Sun Mar 24 02:31:38 2024
print("Printing the flag...")
print("picoCTF{t3@mw0rk_", end='')⏎                                                                                                                                                                                                           ~/p/g/c/drop-in   feature/part-1  git checkout feature/part-2                                                                                                                                                    Sun Mar 24 02:31:40 2024
Switched to branch 'feature/part-2'
 ~/p/g/c/drop-in   feature/part-2  cat flag.py                                                                                                                                                                    Sun Mar 24 02:31:55 2024
print("Printing the flag...")

print("m@k3s_th3_dr3@m_", end='')⏎                                                                                                                                                                                                            ~/p/g/c/drop-in   feature/part-2  git checkout feature/part-3                                                                                                                                                    Sun Mar 24 02:31:57 2024
Switched to branch 'feature/part-3'
 ~/p/g/c/drop-in   feature/part-3  cat flag.py                                                                                                                                                                    Sun Mar 24 02:32:02 2024
print("Printing the flag...")

print("w0rk_6c06cec1}")
 ~/p/g/c/drop-in   feature/part-3    
```
 
 
 picoCTF{t3@mw0rk_m@k3s_th3_dr3@m_w0rk_6c06cec1}
 

---



binhexa
 |  | 100 points
Tags: 
AUTHOR: NANA AMA ATOMBO-SACKEY

Description
How well can you perfom basic binary operations?
Start searching for the flag here nc titan.picoctf.net 49964


picoCTF{b1tw^3se_0p3eR@tI0n_su33essFuL_d6f8047e}


 !  ~/p/general_skills  nc titan.picoctf.net 49964                                                                                                                                                         27.7s  Sun Mar 24 02:42:02 2024

Welcome to the Binary Challenge!"
Your task is to perform the unique operations in the given order and find the final result in hexadecimal that yields the flag.

Binary Number 1: 10001011
Binary Number 2: 11111000


Question 1/6:
Operation 1: '|'
Perform the operation on Binary Number 1&2.
Enter the binary result: 11111011
Correct!

Question 2/6:
Operation 2: '*'
Perform the operation on Binary Number 1&2.
Enter the binary result: 10001000
Incorrect. Try again
Enter the binary result: 11101110000
Incorrect. Try again
Enter the binary result: 11101110000'

Incorrect input. Provide the right input
Enter the binary result: 11101110000
Incorrect. Try again
Enter the binary result: 01000011010101000
Correct!

Question 3/6:
Operation 3: '<<'
Perform a left shift of Binary Number 1 by 1 bits.
Enter the binary result: 000100010110
Correct!

Question 4/6:
Operation 4: '+'
Perform the operation on Binary Number 1&2.
Enter the binary result: 0110000011
Correct!

Question 5/6:
Operation 5: '&'
Perform the operation on Binary Number 1&2.
Enter the binary result:  10001000
Correct!

Question 6/6:
Operation 6: '>>'
Perform a right shift of Binary Number 2 by 1 bits .
Enter the binary result: 01111100
Correct!

Enter the results of the last operation in hexadecimal: 30 31 31 31 31 31 30 30

Incorrect input. Provide the right input!

Enter the results of the last operation in hexadecimal: 303131313131313030
Incorrect answer!

Enter the results of the last operation in hexadecimal: 7C

Correct answer!
The flag is: picoCTF{b1tw^3se_0p3eR@tI0n_su33essFuL_d6f8047e}


---





Scan Surprise
 |  |  | 50 points
Tags: 
AUTHOR: JEFFERY JOHN

Description
I've gotten bored of handing out flags as text. Wouldn't it be cool if they were an image instead?
You can download the challenge files here:
challenge.zip
Additional details will be available after launching your challenge instance.



https://artifacts.picoctf.net/c_atlas/2/challenge.zip

picoCTF{p33k_@_b00_b5ce2572}

scan the qr and get the flag

---

Verify
 |  |  | 50 points
Tags: 
AUTHOR: JEFFERY JOHN

Description
People keep trying to trick my players with imitation flags. I want to make sure they get the real thing! I'm going to provide the SHA-256 hash and a decrypt script to help you know that my flags are legitimate.
You can download the challenge files here:
challenge.zip
Additional details will be available after launching your challenge instance.

https://artifacts.picoctf.net/c_rhea/11/challenge.zip


./d.sh files/ | grep -v "This flag is fake! Keep looking!" 


picoCTF{trust_but_verify_8eee7195}

modified script 

```
#!/bin/bash

# Function to decrypt a file
decrypt_file() {
    local file="$1"
    if openssl enc -d -aes-256-cbc -pbkdf2 -iter 100000 -salt -in "$file" -k picoCTF; then
        echo "Decrypted contents of '$file':"
    else
        echo "Error: Failed to decrypt '$file'. This flag is fake! Keep looking!"
    fi
}

# Recursive function to decrypt all files in a directory
decrypt_files_recursive() {
    local directory="$1"
    for file in "$directory"/*; do
        if [ -f "$file" ]; then
            decrypt_file "$file"
        elif [ -d "$file" ]; then
            decrypt_files_recursive "$file"
        fi
    done
}

# Check if the user provided a directory name as an argument
if [ $# -eq 0 ]; then
    echo "Expected usage: decrypt.sh <directory>"
    exit 1
fi

# Store the provided directory name in a variable
directory="$1"

# Check if the provided argument is a directory
if [ ! -d "$directory" ]; then
    echo "Error: '$directory' is not a valid directory."
    exit 1
fi

# Decrypt files in the specified directory
decrypt_files_recursive "$directory"
```





--------------------------------------------------------------------------------------------------------------------------------------------------------

CanYouSee
 |  |  | 100 points
Tags: 
AUTHOR: MUBARAK MIKAIL

Description
How about some hide and seek?
Download this file here.


https://artifacts.picoctf.net/c_titan/5/unknown.zip



download the zip file

unzip it there is a png image


use exiftool see the meta data you find a base 64 decode it get the flag


```
 ~/p/f/can_you_see  exiftool ukn_reality.jpg                                                                                                       Mon Mar 25 01:25:43 2024
ExifTool Version Number         : 12.67
File Name                       : ukn_reality.jpg
Directory                       : .
File Size                       : 2.3 MB
File Modification Date/Time     : 2024:02:16 04:10:17+05:30
File Access Date/Time           : 2024:02:16 04:10:17+05:30
File Inode Change Date/Time     : 2024:03:25 01:25:41+05:30
File Permissions                : -rw-r--r--
File Type                       : JPEG
File Type Extension             : jpg
MIME Type                       : image/jpeg
JFIF Version                    : 1.01
Resolution Unit                 : inches
X Resolution                    : 72
Y Resolution                    : 72
XMP Toolkit                     : Image::ExifTool 11.88
Attribution URL                 : cGljb0NURntNRTc0RDQ3QV9ISUREM05fNGRhYmRkY2J9Cg==
Image Width                     : 4308
Image Height                    : 2875
Encoding Process                : Baseline DCT, Huffman coding
Bits Per Sample                 : 8
Color Components                : 3
Y Cb Cr Sub Sampling            : YCbCr4:2:0 (2 2)
Image Size                      : 4308x2875
Megapixels                      : 12.4
 ~/p/f/can_you_see                                                                                                                         255ms  Mon Mar 25 01:26:01 2024
 ~/p/f/can_you_see                                                                                                                         255ms  Mon Mar 25 01:26:11 2024
 ~/p/f/can_you_see  base64 -d cGljb0NURntNRTc0RDQ3QV9ISUREM05fNGRhYmRkY2J9Cg==                                                             255ms  Mon Mar 25 01:26:11 2024
base64: 'cGljb0NURntNRTc0RDQ3QV9ISUREM05fNGRhYmRkY2J9Cg==': No such file or directory
 !  ~/p/f/can_you_see  echo "cGljb0NURntNRTc0RDQ3QV9ISUREM05fNGRhYmRkY2J9Cg==" > b64                                                              Mon Mar 25 01:26:19 2024
 ~/p/f/can_you_see  base64 -d b64                                                                                                                  Mon Mar 25 01:27:17 2024
picoCTF{ME74D47A_HIDD3N_4dabddcb}
```


picoCTF{ME74D47A_HIDD3N_4dabddcb}


--------------------------------------------------------------------------------------------------------------------------------------------------------


Secret of the Polyglot
 |  |  | 100 points
Tags: 
AUTHOR: SYREAL

Description
The Network Operations Center (NOC) of your local institution picked up a suspicious file, they're getting conflicting information on what type of file it is. They've brought you in as an external expert to examine the file. Can you extract all the information from this strange file?
Download the suspicious file here.


https://artifacts.picoctf.net/c_titan/8/flag2of2-final.pdf


part 1 1n_pn9_&_pdf_1f991f77}

part2 picoCTF{f1u3n7_}


picoCTF{f1u3n7_1n_pn9_&_pdf_1f991f77}


flag is dead bcz of previous old file again solving by changeoin the extention to png

------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
interencdec
 |  |  | 50 points
Tags: 
AUTHOR: NGIRIMANA SCHADRACK

Description
Can you get the real meaning from this file.
Download the file here.

https://artifacts.picoctf.net/c_titan/2/enc_flag

picoCTF{caesar_d3cr9pt3d_78250afc}

twice base 64 and the rot19 or caesar ciper you can say

-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------



picoCTF{f1u3n7_1n_pn9_&_pdf_249d05c0}



--------------------------------------------------------------------------------------------------------------------------------------------------------

------------------------------------------------------------------------------------------------------------------------------------------------------------------------


Binary Search
 |  |  | 100 points
Tags: 
AUTHOR: JEFFERY JOHN

Description
Want to play a game? As you use more of the shell, you might be interested in how they work! Binary search is a classic algorithm used to quickly find an item in a sorted list. Can you find the flag? You'll have 1000 possibilities and only 10 guesses.
Cyber security often has a huge amount of data to look through - from logs, vulnerability reports, and forensics. Practicing the fundamentals manually might help you in the future when you have to write your own tools!
You can download the challenge files here:
challenge.zip
ssh -p 63335 ctf-player@atlas.picoctf.net
Using the password 1ad5be0d. Accept the fingerprint with yes, and ls once connected to begin. Remember, in a shell, passwords are hidden!



picoCTF{g00d_gu355_3af33d18}

```
 !  ~/p/g/h/c/drop-in  ssh -p 63335 ctf-player@atlas.picoctf.net                                             Mon Mar 25 12:46:48 2024
The authenticity of host '[atlas.picoctf.net]:63335 ([18.217.83.136]:63335)' can't be established.
ED25519 key fingerprint is SHA256:M8hXanE8l/Yzfs8iuxNsuFL4vCzCKEIlM/3hpO13tfQ.
This key is not known by any other names.
Are you sure you want to continue connecting (yes/no/[fingerprint])? yes
Warning: Permanently added '[atlas.picoctf.net]:63335' (ED25519) to the list of known hosts.
ctf-player@atlas.picoctf.net's password: 
Welcome to the Binary Search Game!
I'm thinking of a number between 1 and 1000.
Enter your guess: 500
Higher! Try again.
Enter your guess: 600
Lower! Try again.
Enter your guess: 550
Higher! Try again.
Enter your guess: 560
Higher! Try again.
Enter your guess: 570
Higher! Try again.
Enter your guess: 580
Lower! Try again.
Enter your guess: 575
Lower! Try again.
Enter your guess: 574
Lower! Try again.
Enter your guess: 573
Lower! Try again.
Enter your guess: 572
Congratulations! You guessed the correct number: 572
Here's your flag: picoCTF{g00d_gu355_3af33d18}
Connection to atlas.picoctf.net closed.
```

---

endianness
 |  |  | 200 points
Tags: 
AUTHOR: NANA AMA ATOMBO-SACKEY

Description
Know of little and big endian?
nc titan.picoctf.net 65485. Source
```
Welcome to the Endian CTF!
You need to find both the little endian and big endian representations of a word.
If you get both correct, you will receive the flag.
Word: trvcs
Enter the Little Endian representation: 73 63 76 72 74
Incorrect Little Endian representation. Try again!
Enter the Little Endian representation: Incorrect Little Endian representation. Try again!
Enter the Little Endian representation: Incorrect Little Endian representation. Try again!
Enter the Little Endian representation: Incorrect Little Endian representation. Try again!
Enter the Little Endian representation: Incorrect Little Endian representation. Try again!
Enter the Little Endian representation: 7363767274
Correct Little Endian representation!
Enter the Big Endian representation: 7472766373
Correct Big Endian representation!
Congratulations! You found both endian representations correctly!
Your Flag is: picoCTF{3ndi4n_sw4p_su33ess_817b7cfe}
```

understand and input the number using googling 



---

dont-you-love-banners
 |  |  | 300 points
Tags: 
AUTHOR: LOIC SHEMA / SYREAL

Description
Can you abuse the banner?
Additional details will be available after launching your challenge instance.

---

dont-you-love-banners
 |  |  | 300 points
Tags: 
AUTHOR: LOIC SHEMA / SYREAL

Description
Can you abuse the banner?
The server has been leaking some crucial information on tethys.picoctf.net 51918. Use the leaked information to get to the server.
To connect to the running application use nc tethys.picoctf.net 53635. From the above information abuse the machine and find the flag in the /root directory.


SSH-2.0-OpenSSH_7.6p1 My_Passw@rd_@1234