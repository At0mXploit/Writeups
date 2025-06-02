# Solution

```python
from sys import exit
from Crypto.Util.number import bytes_to_long, inverse
from setup import get_primes

e = 65537

def gen_key(k):
    """
    Generates RSA key with k bits
    """
    p,q = get_primes(k//2)
    N = p*q
    d = inverse(e, (p-1)*(q-1))

    return ((N,e), d)

def encrypt(pubkey, m):
    N,e = pubkey
    return pow(bytes_to_long(m.encode('utf-8')), e, N)

def main(flag):
    pubkey, _privkey = gen_key(1024)
    encrypted = encrypt(pubkey, flag) 
    return (pubkey[0], encrypted)

if __name__ == "__main__":
    flag = open('flag.txt', 'r').read()
    flag = flag.strip()
    N, cypher  = main(flag)
    print("N:", N)
    print("e:", e)
    print("cyphertext:", cypher)
    exit()

```

```bash
╰─[:)] %  nc verbal-sleep.picoctf.net 51510
N: 20675446621924293188247451185532354735013266576368974041911367365015106592566410374445493536514416226339953497702850034215430155362056315028021254482256322
e: 65537
cyphertext: 12357952871467621851244488278693802784538351705070260138661153519752311871502419292395213330724710094182483527650797719801599168946369217379291450067541693
```


- **n**: The modulus, the product of two prime numbers (**p** and **q**).
    
- **e**: The public exponent, typically chosen as a small odd number like 65537.
    
- **p**: A prime number used in the key generation process.
    
- **q**: Another prime number used in the key generation process.
    
- **d**: The private exponent, which is the modular inverse of **e** modulo **(p-1)(q-1)**.
    
- **phi(n)**: The Euler’s totient function of **n**, which is **(p-1)(q-1)**.

```python
from sympy import factorint, mod_inverse

# The given values
N = 20675446621924293188247451185532354735013266576368974041911367365015106592566410374445493536514416226339953497702850034215430155362056315028021254482256322
e = 65537
ciphertext = 12357952871467621851244488278693802784538351705070260138661153519752311871502419292395213330724710094182483527650797719801599168946369217379291450067541693

# Step 1: Factorize N to find p and q
factors = factorint(N)
p, q = factors.keys()
print(f"p: {p}\nq: {q}")

# Step 2: Compute Euler's Totient Function φ(N)
phi_N = (p - 1) * (q - 1)
print(f"φ(N): {phi_N}")

# Step 3: Compute the private key d
d = mod_inverse(e, phi_N)
print(f"Private key d: {d}")

# Step 4: Decrypt the ciphertext using the formula plaintext = ciphertext^d % N
plaintext = pow(ciphertext, d, N)
print(f"Decrypted plaintext (in integer form): {plaintext}")

# Optionally, if you expect the plaintext to be a string, you can convert it from integer to bytes:
# For example, assuming it's a UTF-8 encoded string
plaintext_bytes = plaintext.to_bytes((plaintext.bit_length() + 7) // 8, byteorder='big')
try:
    plaintext_str = plaintext_bytes.decode('utf-8')
    print(f"Decrypted plaintext (string): {plaintext_str}")
except UnicodeDecodeError:
    print("Decrypted plaintext is not a valid UTF-8 string")

```

- `picoCTF{tw0_1$_pr!m3625a858b}`

---
