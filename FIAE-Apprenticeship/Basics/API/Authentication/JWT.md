# JSON Web Tokes
---

## What is a JWT?

JWT is an open standard (RFC7519) that defines a compact and self-contained way for securely transmitting information between to applications as a [[JSON]] object. This information can be verified and trusted because it is digitally signed. 
JWTs can be signed using a secret (with the [[HMAC]] algorithm) or a public/private key pair using [[RSA]] or [[ECDSA]].


## When to use JWTs

There are two main scenarios where using a JWT can prove itself to be quite useful:
1. [[API Authentication|Authentication]] This is the most common scenario for using JWT. Once the user, is logged in, each subsequent request will include the JWT, allowing the user to access routes, services and resources that are permitted with that token.
2. **Information Exchange** JWTs are a good way of securely transmitting information between applications. Because JWTs can be signed, using public/private key pairs, you can be sure the senders are who they say they are. 


## The structure of a JWT

In its compact form, JWTs consist of three parts separated by dots, which are:
- Header
- Payload
- Signature

Therefore, a JWT typically looks like the following:

	<xxxxx.yyyyy.zzzzz

### Header

The header *typically* consists of two parts: the type of the token, which is JWT, and the signing algorithm being used, such as HMAC, SHA256 or RSA
As an example:
>{ 
>	"alg": "HS256", 
>	"typ": "JWT" 
>}

Then, this [[JSON]] is [[Base64URL]] encoded to form the first part of the JWT.


### Payload

The second part of the token is the payload, which contains the claims. Claims are statements about an entity (typically, the user) and additional data. There are three types of claims: _registered_, _public_, and _private_ claims.

- **Registered Claims** These are a set of predefined claims which are not mandatory but recommended, to provide a set of useful, interoperable claims. Some of them are: **iss** (issuer), **exp** (expiration time), **sub** (subject), **aud** (audience), and others.
    
    > Notice that the claim names are only three characters long as JWT is meant to be compact.
    
- **Public claims**: These can be defined at will by those using JWTs. But to avoid collisions they should be defined in the IANA JSON Web Token Registry or be defined as a URI that contains a collision resistant namespace.
    
- **Private claims**: These are the custom claims created to share information between parties that agree on using them and are neither _registered_ or _public_ claims.
    

An example payload could be:

```
{
  "sub": "1234567890",
  "name": "John Doe",
  "admin": true
}
```

The payload is then [[Base64Url]] encoded to form the second part of the JSON Web Token.


### Signature

To create the signature part you have to take the encoded header, the encoded payload, a secret, the algorithm specified in the header, and sign that.

For example if you want to use the HMAC SHA256 algorithm, the signature will be created in the following way:

```
HMACSHA256(
  base64UrlEncode(header) + "." +
  base64UrlEncode(payload),
  secret)
```

The signature is used to verify the message wasn't changed along the way, and, in the case of tokens signed with a private key, it can also verify that the sender of the JWT is who it says it is.

