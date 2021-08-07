## Encryption, Decryption & Hacking
### Encrypting a message
The Caesar Cipher is a simple substitution cipher which replaces each original letter with a different letter in the alphabet by shifting the alphabet by a certain amount.  
- A Simple text message
```
SECRET MEETING AT THE PALACE
```
- Here's what that might look like encrypted:
```
YKIXKZ SKKZOTM GZ ZNK VGRGIK
```
### Decrypting a message
- Here's a ecrypted message
```
FURVV WKH UXELFRQ
```
- The corresponding simpe text would look like
```
CROSS THE RUBICON
```
### Cracking the cipher

There are three main techniques that could use to crack cipher wo=ithou knowing the shift:
- Frequency analysis
- Known plaintext
- Brute force.

### Frequency analysis

Human languages tend to use some letters more than others. For example, "E" is the most popular letter in the English language. We can analyze the frequency of the characters in the message and identify the most likely "E" and narrow down the possible shift amounts based on that.

### Known plaintext
Another term for the original unencrypted message is plaintext. If the enemy already knew some part of the plaintext, it will be easier for them to crack the rest of the encrypted version.
For example, messages tend to start with similar beginnings. In WWII, encrypted German messages always started with a weather forecast, which ultimately made them easier for British mathematician Alan Turing to crack.

### Brute Force
There are only 25 possible shifts (not 26 — why not?). We could take some time to try out each of them and find one that yielded a sensible message. They wouldn't even need to try the shifts on the entire message, just the first word or two.
