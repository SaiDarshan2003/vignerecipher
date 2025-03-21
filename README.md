## EX.NO: 4 Vigenere Cipher

## AIM:
To develop a simple C program to implement Vigenere Cipher.

## DESIGN STEPS:
Step 1:
Design of Vigenere Cipher algorithnm

Step 2:
Implementation using C or pyhton code

Step 3:
Testing algorithm with different key values. 

## PROGRAM:
```
#include <stdio.h>
#include <string.h>
#include <ctype.h>
void encryptVigenere(char *plaintext, char *key, char *ciphertext) {
    int textLen = strlen(plaintext);
    int keyLen = strlen(key);
    int i, j;
    for (i = 0, j = 0; i < textLen; i++) {
        if (isalpha(plaintext[i])) { 
            char base = isupper(plaintext[i]) ? 'A' : 'a';
            char keyBase = isupper(key[j % keyLen]) ? 'A' : 'a';
            ciphertext[i] = ((plaintext[i] - base + (key[j % keyLen] - keyBase)) % 26) + base;
            j++; // Move to next letter in key
        } else {
            ciphertext[i] = plaintext[i]; 
        }
    }
    ciphertext[i] = '\0'; 
}
```

## OUTPUT:

![image](https://github.com/user-attachments/assets/02811bc2-ff87-4755-9f2b-e426e63d0d29)

## RESULT:
The program is executed successfully




