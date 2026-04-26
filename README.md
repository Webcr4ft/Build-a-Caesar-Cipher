Caesar Cipher Project (Python)

Overview

This project is a simple implementation of the Caesar Cipher, a classic encryption technique where each letter in a text is shifted a fixed number of places in the alphabet.

It supports both:

Encryption (encoding text)

Decryption (decoding text)


The implementation also includes support for ROT13, a special case of the Caesar cipher.



How It Works

The cipher works by shifting each letter in the alphabet by a given number called the shift value.

For example, with a shift of 3:

A → D

B → E

C → F


The shift wraps around the alphabet, so Z loops back to A.



ROT13 Explained

ROT13 (Rotate by 13) is a special Caesar cipher where the shift value is 13.

Why 13?

The English alphabet has 26 letters

13 is exactly half of 26

This means each letter maps to another letter halfway across the alphabet


Example:

A ↔ N

B ↔ O

C ↔ P


Important Feature:

ROT13 is self-inverse, meaning:

Applying ROT13 twice returns the original text


So:

Encrypting with shift 13

Decrypting with shift 13 leads back to the original message.


Functions

caesar(text, shift, encrypt=True)

Core function that:

Validates shift value (must be between 1 and 25)

Creates shifted alphabet mapping

Applies transformation using str.maketrans()


Parameters:

text: The message to encrypt or decrypt

shift: Number of positions to shift

encrypt: If False, performs decryption




encrypt(text, shift)

Wrapper function for encryption.

Example:

encrypt("hello", 3)



decrypt(text, shift)

Wrapper function for decryption.

Example:

decrypt("khoor", 3)



Example Usage

encrypted_text = 'Pbhertr vf shbav va hayvxryl cynprf.'
print(encrypted_text)

decrypted_text = decrypt(encrypted_text, 13)
print(decrypted_text)



Key Features

Supports uppercase and lowercase letters

Preserves non-alphabet characters (spaces, punctuation)

Input validation for shift values

Clean reusable functions

Includes ROT13 support



Summary

This project demonstrates a classic cryptography technique and shows how simple mathematical transformations can be used to encode and decode messages efficiently in Python.
