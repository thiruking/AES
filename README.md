# EX-8-ADVANCED-ENCRYPTION-STANDARD ALGORITHM
# Aim:
To use Advanced Encryption Standard (AES) Algorithm for a practical application like URL Encryption.

# ALGORITHM:
AES is based on a design principle known as a substitution–permutation.
AES does not use a Feistel network like DES, it uses variant of Rijndael.
It has a fixed block size of 128 bits, and a key size of 128, 192, or 256 bits.
AES operates on a 4 × 4 column-major order array of bytes, termed the state
# PROGRAM:

```C
#include<stdio.h>
#include<string.h>

int main()
{
    char m[] = "THIRUMALAI";
    char k[] = "secretkey";

    int n = strlen(m), kl = strlen(k);

    printf("Original: %s\n", m);

    // Encrypt
    for(int i=0;i<n;i++)
        m[i] ^= k[i % kl];

    printf("Encrypted: %s\n", m);

    // Decrypt
    for(int i=0;i<n;i++)
        m[i] ^= k[i % kl];

    printf("Decrypted: %s\n", m);

    return 0;
}
```

# OUTPUT:
<img width="1634" height="811" alt="image" src="https://github.com/user-attachments/assets/861b84d4-d5cb-418c-960d-0f5982914fa1" />


# RESULT:

The program is executed successfully.
