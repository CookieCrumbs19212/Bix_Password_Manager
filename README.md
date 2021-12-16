# Bix_Password_Manager

### **Bix Development Status Indicator:** 🔴
🔴: Fatal flaws or bugs detected.<br/>
🟡: New update in development.<br/>
🟢: Healthy Release.<br/>

**ATTENTION:** DO NOT USE THIS CODE. THIS REPO IS STILL IN DEVELOPMENT, IT IS INFESTED WITH BUGS AND DESIGN FLAWS.

## What is Bix?

Bix is a console-based Account Credentials Manager.  
It encrypts and safely stores account credentials with your choice of AES flavor (128-bit, 192-bit or 256-bit).


## Important Definitions

1. `Master Password` : The Master Password is used to encrypt and decrypt the vault where all your account credentials are stored. And so, it is important to keep your Master Password safe.


## How are the Credentials stored?

1. The `username` and `password` are appended together and separated by a whitespace to create the `plaintext`. <br/>Hence the `plaintext` will look like this: "`username password`"  
2. The *PLAINTEXT* is then padded using `PKCS5`.  
3. Next, the *PLAINTEXT* is encrypted using `AES-128 bit` in `CBC` mode to get the *CIPHERTEXT*.  
4. Finally, the CIPHERTEXT is encoded in Base64 and stored in the credentials.csv file, along with the ACCOUNT NAME, Initialization Vector (IV), SALT and SHA256 hash of the SECRET KEY.  


## A Piece of Friendly Advice
When it comes to safely (in the case of some people I know, "unsafely") storing passwords and other sensitive information, everyone has their own approach; and no matter which "foolproof" method you adopt, there will always be some form of risk involved.  
  
Bix is purely for convenience, and in my opinion, you must never solely rely on Bix (or any other digital password manager) to store all your account credentials for you.  
  
Instead, I would encourage you to adopt the simple hybrid solution:  
**A digital password manager for convenience and a tangible password journal for confidence.**  
This way, you're not putting all your eggs in one basket. 
