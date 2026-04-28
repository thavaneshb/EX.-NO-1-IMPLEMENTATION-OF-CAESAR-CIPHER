# EX. NO: 1(A) : IMPLEMENTATION OF CAESAR CIPHER

## AIM:
To implement the simple substitution technique named Caesar cipher using C language.

## ALOGORITHM:

STEP-1: Read the plain text from the user.

STEP-2: Read the key value from the user.

STEP-3: If the key is positive then encrypt the text by adding the key with each character in the plain text.

STEP-4: Else subtract the key from the plain text.

STEP-5: Display the cipher text obtained above.

## PROGRAM:
```

def caesar_cipher_encrypt(text, key):
    cipher = ""
    for ch in text:
        if ch.isupper():
            cipher += chr((ord(ch) - ord('A') + key) % 26 + ord('A'))
        elif ch.islower(): 
            cipher += chr((ord(ch) - ord('a') + key) % 26 + ord('a'))
        else:
            cipher += ch  
    return cipher
def caesar_cipher_decrypt(cipher, key):
    plain = ""
    for ch in cipher:
        if ch.isupper():  
            plain += chr((ord(ch) - ord('A') - key) % 26 + ord('A'))
        elif ch.islower():  
            plain += chr((ord(ch) - ord('a') - key) % 26 + ord('a'))
        else:
            plain += ch
    return plain
plain = input("Enter the plain text: ")
key = int(input("Enter the key value: "))

print("\nPLAIN TEXT:", plain)

cipher = caesar_cipher_encrypt(plain, key)
print("ENCRYPTED TEXT:", cipher)

decrypted = caesar_cipher_decrypt(cipher, key)
print("DECRYPTED TEXT:", decrypted)

```

## OUTPUT:

<img width="1745" height="1077" alt="image" src="https://github.com/user-attachments/assets/b55fc9e2-6b71-4bde-9c9b-1b8afe76b90b" />


## RESULT :
 Thus the implementation of ceasar cipher had been executed successfully.
