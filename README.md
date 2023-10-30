# Text Encryption and Decryption using Multiple Ciphers

## Description
This project delves deep into the theories and mathematical underpinnings of four classical ciphers: Caesar, Affine, Vigenere, and Rail Fence Technique. Each cipher has its unique approach and history, and understanding their algorithms provides a comprehensive insight into their encryption and decryption processes.



## 1. Caesar Cipher

### Theory
The Caesar Cipher, named after Julius Caesar, is one of the simplest and most widely recognized encryption techniques. It's a substitution cipher where each character in the plaintext is shifted a certain number of places down or up the alphabet.

### Encryption Algorithm
**Formula**: 
```
E_n(x) = (x + n) mod 26
```

### Decryption Algorithm
**Formula**: 
```
D_n(x) = (x - n) mod 26
```



## 2. Affine Cipher

### Theory
The Affine Cipher is a type of monoalphabetic substitution cipher. It encrypts one letter at a time and employs arithmetic operations from modular arithmetic, ensuring each letter maps to another unique letter.

### Encryption Algorithm
**Formula**: 
```
E_{a,b}(x) = (ax + b) mod 26
```

### Decryption Algorithm
**Formula**: 
```
D_{a,b}(x) = a^{-1}(x - b) mod 26
```


## 3. Vigenere Cipher

### Theory
The Vigenere Cipher is a method of encrypting alphabetic text using a simple form of polyalphabetic substitution. Unlike the Caesar Cipher which shifts all letters by a fixed number, the Vigenere Cipher shifts each letter according to a keyword.

### Encryption Algorithm
**Formula**: 
```
E_k(P_i) = (P_i + K_i) mod 26
```

### Decryption Algorithm
**Formula**: 
```
D_k(C_i) = (C_i - K_i + 26) mod 26
```



## 4. Rail Fence Technique Cipher

### Theory
The Rail Fence Cipher is a type of transposition cipher that rearranges the letters of the plaintext to encrypt. It writes the message in a zig-zag pattern between 'rails' and then reads off each row.


### Rail Fence Technique Visualization

For a clearer visualization of the Rail Fence Technique, consider the example "oriab hjaih hja" with a key of 3.

### Encryption:

1. Write down the message in a zig-zag pattern along three lines (rails):
   ```
   o . . . r . . . i . . . a . . . b . . . c
   . h . j . v . d . u . c . p .
   . . . . . . . . . . . . . . . . . . . . .
   ```

2. Combine each row to get the encrypted message: "oriabc hj vducp"

### Decryption:

1. Mark positions where characters should be in the zig-zag pattern:
   ```
   o . . . * . . . * . . . * . . . * . . . *
   . * . * . * . * . * . * . * .
   . . . . . . . . . . . . . . . . . . . . .
   ```

2. Fill the positions with the characters from the encrypted message in the order they appear.

3. Read the message row by row in a zig-zag pattern to get the decrypted message: "oriab hjaih hja"

---

The Rail Fence Technique focuses on rearranging the position of characters rather than substituting them. The visualization helps to understand how characters are positioned in rails, providing a clear idea of how the encryption and decryption processes work.



## Example
Encrypting the text "ramzy fariz fam":

1. **Caesar Cipher (shift 3)**
   - Encrypted: "udpac idulc idp"
2. **Affine Cipher (a = 5, b = 8)**
   - Encrypted: "ifpan ulpnp uli"
3. **Vigenere Cipher (key = 'key')**
   - Encrypted: "oriab hjaih hja"
4. **Rail Fence Cipher (key = 3)**
   - Encrypted: "oriabc hj vducp"

```plaintext
Input your text: ramzy fariz fam
Encrypted Text : oriabc hj vducp
Decrypted Text : ramzy fariz fam
```
## Example Decryption

Using the text "oriabc hj vducp":

1. **Rail Fence Cipher (key = 3)**
   - Visualization:
     ```
     o . . . r . . . i . . . a . . . b . . . c
     . h . j . v . d . u . c . p .
     . . . . . . . . . . . . . . . . . . . . .
     ```
   - Decrypted: "oriab hjaih hja"

2. **Vigenere Cipher (key = 'key')**
   - Decrypted: "ifpan ulpnp uli"

3. **Affine Cipher (a = 5, b = 8)**
   - Decrypted: "udpac idulc idp"

4. **Caesar Cipher (shift 3)**
   - Decrypted: "ramzy fariz fam"

```plaintext
Input your encrypted text: oriabc hj vducp
Decrypted Text: ramzy fariz fam
```



## Conclusion
Each of the ciphers mentioned above has its strengths and weaknesses, and their combined usage can provide stronger encryption. Understanding the mathematical and algorithmic principles behind these ciphers is crucial for both cryptography enthusiasts and professionals aiming to implement or break these ciphers.




