## Authentication 👋 👩🏻‍💻 
![auth](./assest/auth.png)<br>
<br>

- Cryptographic hash algorithms MD5, SHA1, SHA256, SHA512, SHA-3 are general purpose hash functions.

- designed to calculate a digest of huge amounts of data in as short a time as possible.

- Hashing is the greatest way for protecting passwords and considered to be pretty safe for ensuring the integrity of data or password.

-----------------------
## 👀 📝 Problem With Cryptographic Hash Algorithm: 👀 📝
1. Brute Force attack
2. Hash Collision attack

-----------------------
## The best way: 👌👌
* PBKDF2
* BCrypt

** both of these algorithms use a technique called Key Stretching.

- Bcrypt is an adaptive hash function based on the Blowfish symmetric block cipher cryptographic algorithm and introduces a work factor (also known as security factor), which allows you to determine how expensive the hash function will be.

- This work factor value determines how slow the hash function will be, means different work factor will generate different hash values in different time span, which makes it extremely resistant to brute force attacks. When computers become faster next year we can increase the work factor to balance it out i.e. to make the attack slower.
<br>

--------------------------------------
## Basic access authentication: ✔️
In the context of an HTTP transaction, basic access authentication is a method for an HTTP user agent (e.g. a web browser) to provide a user name and password when making a request. In basic HTTP authentication, a request contains a header field in the form of Authorization: Basic credentials, where credentials is the Base64 encoding of ID and password joined by a single colon :.

<br>

## Features: ✔️ ✔️
HTTP Basic authentication (BA) implementation is the simplest technique for enforcing access controls to web resources because it does not require cookies, session identifiers, or login pages; rather, HTTP Basic authentication uses standard fields in the HTTP header.<br>

## Security: 🔐🔐
The BA mechanism does not provide confidentiality protection for the transmitted credentials.

They are merely encoded with Base64 in transit and not encrypted or hashed in any way. Therefore, basic authentication is typically used in conjunction with HTTPS to provide confidentiality.
<br>

## Protocol: ✔️ ✔️
1. Server side

WWW-Authenticate: Basic realm="User Visible Realm", charset="UTF-8"

2. Client side

username:password or QWxhZGRpbjpvcGVuIHNlc2FtZQ==

Authorization: Basic QWxhZGRpbjpvcGVuIHNlc2FtZQ==





<br>

[Back to the main page  ✔️](README.md)
