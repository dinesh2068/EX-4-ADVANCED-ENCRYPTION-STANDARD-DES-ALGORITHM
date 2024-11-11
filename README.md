# EX-8-ADVANCED-ENCRYPTION-STANDARD-DES-ALGORITHM

## Aim:
  To use Advanced Encryption Standard (AES) Algorithm for a practical application like URL Encryption.

## ALGORITHM: 
  1. AES is based on a design principle known as a substitution–permutation. 
  2. AES does not use a Feistel network like DES, it uses variant of Rijndael. 
  3. It has a fixed block size of 128 bits, and a key size of 128, 192, or 256 bits. 
  4. AES operates on a 4 × 4 column-major order array of bytes, termed the state

## PROGRAM: 
```
def xor_encrypt_decrypt(input_string, key):
    input_len = len(input_string)
    key_len = len(key)
    result = ""
    for i in range(input_len):
        result += chr(ord(input_string[i]) ^ ord(key[i % key_len]))
    return result
def main():
    url = input("Enter the URL:")
    key = input(" Enter the Key: ") # Simple key for XOR encryption
    print("Original URL:", url)
    encrypted_url = xor_encrypt_decrypt(url, key)
    print("Encrypted URL:", encrypted_url)
    decrypted_url = xor_encrypt_decrypt(encrypted_url, key)
    print("Decrypted URL:", decrypted_url)
main()
```
## OUTPUT:
![Screenshot 2024-11-11 102456](https://github.com/user-attachments/assets/e31d05ba-9a96-41c9-9446-0f20b52a10b8)

## RESULT: 
The Program is executed Successfully.
