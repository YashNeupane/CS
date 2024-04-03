I will generate SSH keys and learn how to use them for authentication, encryption, and integrity.

I will use the ssh-keygen command. There are a lot of different options, but for today, we'll generate 4096-bit SSH RSA public and private keys.
  What is the ssh-Keygen command? 
  - 
Run ssh-keygen -t rsa -b 4096 -C "CYB101 Ubuntu Key"
Commands breakdown:

ssh-keygen = the utility used to generate the key pair
-t rsa = specifies the type of key to create (e.g., rsa)
-C "CYB101 Ubuntu Key" = provides custom key comment (which will be appended at the end of the public key).
Usually an email address is used as a comment, but this time we're labeling it with the machine we'll use it on.
Think of it like a label for your key, so you don't mix it up with other keys!
