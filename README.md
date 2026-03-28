# EX-NO14-HASH-ALGORITHM
## NAME: PRIYADHARSHINI P
## REGISTER NUMBER: 212224040252
## DATE: 17-03-2026

## AIM:
To implement HASH ALGORITHM

## ALGORITHM:

1. Hash Algorithm is used to convert input data (message) into a fixed-size string, typically a hash value, which uniquely represents the original data.

2. Initialization:
   - Choose a hash function \( H \) (e.g., SHA-256, MD5, etc.).
   - The message \( M \) to be hashed is input.

3. Message Preprocessing:
   - Break the message \( M \) into fixed-size blocks. If necessary, pad the message to make it compatible with the block size required by the hash function.
   - For example, in SHA-256, the message is padded to ensure that its length is a multiple of 512 bits.

4. Hash Calculation:
   - Process the message block by block, applying the hash function \( H \) iteratively to produce an intermediate hash value.
   - For SHA-256, each block is processed through a series of logical operations, bitwise manipulations, and modular additions.

5. Output:
   - After all blocks are processed, the final hash value (digest) is produced, which is a fixed-size output (e.g., 256-bit for SHA-256).
   - The resulting hash is unique to the input message, meaning even a small change in the message will result in a completely different hash.

6. Security: The strength of the hash algorithm lies in its collision resistance, ensuring that it is computationally infeasible to find two different messages that produce the same hash value.


## Program:
```
#include <stdio.h>

int main(){
    char m[100]; unsigned char h=0; int i;

    scanf("%s",m);

    for(i=0;m[i];i++){
        h=h^m[i];
        h+=m[i];
    }

    printf("Hash:%02x",h);
}
```


## Output:
<img width="1328" height="495" alt="image" src="https://github.com/user-attachments/assets/08861d22-7a6c-4798-a0b8-6141217b0061" />



## Result:
The program is executed successfully.
