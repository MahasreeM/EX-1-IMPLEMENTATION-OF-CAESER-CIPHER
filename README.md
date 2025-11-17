## REG.NO:212224110035
## NAME:MAHA SHREE.M
## Exp:1 IMPLEMENTATION OF CAESER CIPHER 

## AIM: 
To encrypt and decrypt the given message by using Caeser Cipher encryption algorithm. 
  
 ## ALGORITHM: 
1. Calculate the length of the plaintext. 
2. For each character in the plaintext:  
 a. Add the key to the character to get the cipher character.  
 b. If the result exceeds 'Z' for uppercase or 'z' for lowercase, subtract 26 to wrap within the  alphabet.  
3. Display the encrypted text.  
4. For decryption, subtract the key from each character of the ciphertext.  
 a. If the result is less than 'A' for uppercase or 'a' for lowercase, add 26 to wrap within the  alphabet.  
5. Display the decrypted text.  

## PROGRAM: 
```
#include <stdio.h>
#include <string.h>
void caesarCipher(char *text, int value) 
{
    for (int i = 0; text[i]; i++) 
    {
        if (text[i] >= 'A' && text[i] <= 'Z')
        text[i] = ((text[i]- 'A' + value) % 26) + 'A';
        
    }
 }
int main() 
{
    char text[] = "MAHA SHREE";
    caesarCipher(text, 3);
    printf("Encrypted Message: %s\n", text);
    caesarCipher(text,-3);
    printf("Decrypted Message: %s\n", text);
    return 0;
    
}
```
## OUTPUT: 
<img width="1452" height="535" alt="image" src="https://github.com/user-attachments/assets/9cf0bf05-2dff-4a5d-8a86-011cba202b98" />

## RESULT: 
The program implementing the Caesar cipher for encryption and decryption has been successfully  executed, and the results have been verified.
