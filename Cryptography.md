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

To deteremine the modulus of  RSA key as a hex string:
openssl rsa -pubin -in key.txt -text -noout
