#### Symmetric encryption
It's based on a shared secret key used for both encryption and decryption.
EX:AES,3DES
#### Asymmetric encryption
It's based on two key, public key and private key while the private key should be very secured the public key can be seen or used by others.
EX: RSA,DSA.

unsalted hashes decoder https://crackstation.net/
###### What is a signature?
It's a hash that checks the validity of some data.

CMS signature is a standardized way to send data+ signature + certificate in one file. 
SOAP signature is a way to send data and signature and optionally certificate. ALL in XML payload. 

To determine the modulus of  RSA key as a hex string:
openssl rsa -pubin -in key.txt -text -noout
Since your private key is in **PKCS#8 PEM format**, it contains **both the private and public key information** internally.
Assignment : to determine the modulus of the RSA key as a hex string, and calculate a signature for that hex string using the key.
step by step procedure:
STEP1: Save the private key
nano private_key.pem
STEP2: Extract the modulus
openssl pkey -in private_key.pem -pubout -text -noout
but remove the 00 and the colon and space.
STEP3: Convert the hex string to binary
echo -n "c61ccf9c8eb27913..." | xxd -r -p > modulus.bin
STEP4: Sign the binary data
openssl dgst -sha256 -sign private_key.pem -out signature.bin modulus.bin
STEP5: Output the signature
xxd -p signature.bin
for base64 > base64 signature.bin
