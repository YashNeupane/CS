#INTRODUCTION

For this project, I will be working with a (fictional) leaked password file, modeled after famous data breaches such as the 2012 LinkedIn Hack and 2016 Yahoo Data Breaches.
In both of these incidents, usernames and hashed passwords were leaked in simple .txt files, making people's private data available to anyone who could crack the hashes.

First, I ran this command [ First, run sudo chown $USER:$USER cp_leak.txt ]

when you run sudo chown $USER:$USER cp_leak.txt, you are changing the ownership of the file cp_leak.txt to the current user and their associated group.

This can be useful if the file was previously owned by another user or if you want to ensure that you have the appropriate permissions to access or modify the file.

Then, The command john --show cp_leak.txt is used to display the cracked passwords from the file cp_leak.txt using the John the Ripper password cracking tool.

I have 706 passwords left to crack in total 

Using the following commands -> I was able to crack 294 passwords

Command #1: a john command using a different wordlist (not lower.lst)

 John -–wordlist=rockyou.txt cp_leak.txt

Command #2: a john command using a built-in ruleset

John -–wordlist=rockyou.txt cp_leak.txt --rules=Jumbo

John -–wordlist=rockyou.txt cp_leak.txt --rules=ShiftToggle

Command #3: a john command using a custom mask
john --mask=?d?a?z


![Screenshot 2024-04-02 202726](https://github.com/YashNeupane/CS/assets/128945418/022ae704-6090-4bbf-afdc-29caf863c348)
