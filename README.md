# EthereumWalletGenerator
Selects private key from random int and uses it to generate public key and wallet. Subsequent plans to add verification and signing. Some code borrowed from Geth's Secp256 elliptic curve.

# According to Ethereum Yellow Paper

random integer selected from [1, secp256k1n − 1].

secp256k1n = 115792089237316195423570985008687907852837564279074904382605163141518161494337 

Pub key genated via: ECDSAPUBKEY(pr ∈ B32) ≡ pu ∈ B64



