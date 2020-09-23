# Class 10 Readings (Sept. 22nd)

## User Modeling

- Protecting the users password by encrpytion, using a hashing algorithm before the password is ever stored. User models that have sensitive info should never be sent to client applications.

## Cryptography

- Ctyptography is the science which studies methods for encoding messages so that they can be read only by a person who knows the secret information required for decoding, called the key; it includes cryptanalysis, the science of decoding encrypted messages without possesing the proper key, and has several other branches.

## Hash Algorithms

- A Cryptographic Hash Algorithm takes a piece of data and produces a hash that is deliberately difficult to reverse. Hash algorithms are used to check the integrity of the data.

## Cypher Algorithms

- Takes a piece of data and a key and produces encrypted data. Later the data can be reversed into the original data by decrypting it using the same key.

## Basic Authorization

- Basic Authorization is a common method used to send a username and password in an HTTP request. The username and password are joined with a ‘:’ then “base64 encoded” and placed after the string ‘Basic ‘. The resulting string is set to the value of an Authorization header.

- In browsers, we get atob and btoa to convert to/from “Base64 Encoding”

```js
let encoded = window.btoa('someusername:P@55w0rD!')
// c29tZXVzZXJuYW1lOlBANTV3MHJEIQ==

let decoded = window.atob('c29tZXVzZXJuYW1lOlBANTV3MHJEIQ==');
// someusername:P@55w0rD!

request({
  method: 'GET',
  url: 'https://api.example.com/login',
  headers: {
    Authorization: `Basic ${encoded}`,
  },
})
.then(handleLogin)
.catch(handleLoginError)
```

## JSON Web Tokens

- JWT is an open standard that defines a compact and self-contained way for securely transmitting information between parties as a JSON object. This information can be verified and trusted because it is digitally signed. 
