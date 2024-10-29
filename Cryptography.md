# Cryptography

## Asymetric Cryptography

```sh
# generate file with random value
openssl rand -out key.bin 64

# encrypt and decrypt message with AES-256-CBC
openssl enc -aes-256-cbc -salt -in message.txt -pass file:./key.bin -out mensagem.txt.encs
openssl enc -aes-256-cbc -d -in mensagem.txt.encs -pass file:./key.bin -out mensagem.txt.decs
```

## Symetric Cryptography

```sh
# generate private and public keys with RSA
openssl genpkey -algorithm rsa -out key.priv.pem
openssl rsa -pubout -in key.priv.pem -out key.pub.pem

# encrypt with public key and decrypt with private key
openssl pkeyutl -encrypt -pubin -inkey key.pub.pem -in message.txt -out message.txt.pub.enc
openssl pkeyutl -decrypt -inkey key.priv.pem -in message.txt.pub.enc -out message.txt.pub.dec

# encrypt with private key and decrypt with private key
openssl pkeyutl -encrypt -inkey key.priv.pem -in message.txt -out message.txt.priv.enc
openssl pkeyutl -decrypt -inkey key.priv.pem -in message.txt.priv.enc -out message.txt.priv.dec
```

## Hashing

```sh
# hash with SHA-256 algorithm
sha256sum message.txt
```

### Show file content

```sh
# display content in hexadecimal
hexdump key.bin

# display content as text
cat message.txt
```

