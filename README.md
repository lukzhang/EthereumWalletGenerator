# EthereumWalletGenerator
Selects private key from random int and uses it to generate public key and wallet. Subsequent plans to add verification and signing. Some code borrowed from Geth's Secp256 elliptic curve.

# According to Ethereum Yellow Paper

random integer selected from [1, secp256k1n − 1].

secp256k1n = 115792089237316195423570985008687907852837564279074904382605163141518161494337 
This number comes from Curve P-256 (p = 2^256 - 2^224 + 2^192 + 2^96 - 1) as defined by Johnson et. al (2001). 

Pub key genated via: ECDSAPUBKEY(pr ∈ B32) ≡ pu ∈ B64

ECDSAPUBKEY and other important functions are defined by Johnson et. al, 2001 (https://web.archive.org/web/20170921160141/http://cs.ucsb.edu/~koc/ccs130h/notes/ecdsa-cert.pdf)

Taking the ECDSAPUBKEY(pr), the value is hashed with Keccak. Then, the right most 160-bits are taken and used as the address. 


