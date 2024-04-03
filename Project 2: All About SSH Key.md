I will generate SSH keys and learn how to use them for authentication, encryption, and integrity.

I will use the ssh-keygen command. There are a lot of different options, but for today, we'll generate 4096-bit SSH RSA public and private keys.
 
What is the ssh-Keygen command? 
  - it's used to generate SSH key pairs, which consist of a public key and a private key.

-> Run ssh-keygen -t rsa -b 4096 -C "Ubuntu Key"

Commands breakdown:
1. ssh-keygen = the utility used to generate the key pair
2. -t rsa = specifies the type of key to create (e.g., rsa)
3. -C "Ubuntu Key" = provides custom key comment (which will be appended at the end of the public key).
Usually an email address is used as a comment. (Think of this like a label for your key, so you don't mix it up with other keys!)

- An SSH key pair that consists of a public key and a private key.
    - The public key will have the .pub extension, and the private key will have no extension.

Encryption with SSH Keys
- We can use SSH keys for asymmetric encryption, where:
    - The public key is used to encrypt a message
    - The private key is used to decrypt it

Encryption with SSH Keys
We can use SSH keys for asymmetric encryption, where:

The public key is used to encrypt a message
The private key is used to decrypt it


We're going to use openssl this time, because it comes with built-in cryptography functions

 | openssl genrsa -out ~/.ssh/privatekey.pem 2048
 | openssl rsa -in  ~/.ssh/privatekey.pem -out ~/.ssh/publickey.pem -pubout -outform PEM

^^^^^^ These commands generate an RSA key pair, consisting of a private key (privatekey.pem) and a corresponding public key (publickey.pem), and save them to files in the ~/.ssh directory.

Next, I create a secret message file called secret.txt.

Run -> echo "MY SECRET MESSAGE" > secret.txt
   - echo "My secret code is I am cool" > secret.txt

























