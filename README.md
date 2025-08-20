## EX. NO: 1 : IMPLEMENTATION OF CAESAR CIPHER
 

## AIM:

To implement the simple substitution technique named Caesar cipher using C language.

## DESCRIPTION:

To encrypt a message with a Caesar cipher, each letter in the message is changed using a simple rule: shift by three. Each letter is replaced by the letter three letters ahead in the alphabet. A becomes D, B becomes E, and so on. For the last letters, we can think of the
alphabet as a circle and "wrap around". W becomes Z, X becomes A, Y bec mes B, and Z
becomes C. To change a message back, each letter is replaced by the one three before it.

## EXAMPLE:



![image](https://github.com/Hemamanigandan/CNS/assets/149653568/eb9c6c43-8c80-4cdd-b9d4-91705a311c79)


## ALGORITHM:

### STEP-1: Read the plain text from the user.
### STEP-2: Read the key value from the user.
### STEP-3: If the key is positive then encrypt the text by adding the key with each character in the plain text.
### STEP-4: Else subtract the key from the plain text.
### STEP-5: Display the cipher text obtained above.


PROGRAM :-

```
Developed by : B.VIMALRAJ
Regitser Number : 212224230304

def caesar_cipher(text, shift, mode='encrypt'):
    result = ""
    if mode == 'decrypt':
        shift = -shift
    for char in text:
        if char.isalpha():
            base = ord('A') if char.isupper() else ord('a')
          
            result += chr((ord(char) - base + shift) % 26 + base)
        else:
            result += char
    return result
Plain_text= "VIMALRAJ"
key = 3

encrypted = caesar_cipher(Plain_text, key, 'encrypt')
decrypted = caesar_cipher(encrypted, key, 'decrypt')

print("Original :", Plain_text)
print("Encrypted:", encrypted)
print("Decrypted:", decrypted)

```

OUTPUT :-

<img width="905" height="726" alt="Screenshot 2025-08-20 092406" src="https://github.com/user-attachments/assets/fec0156f-04cc-480c-9bb2-0aa5d67eba1d" />
