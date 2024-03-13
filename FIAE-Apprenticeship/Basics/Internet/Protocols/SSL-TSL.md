# SSL and TSL
---


## What are SSL and TSL?

Both **TLS** and **SSL** are protocols that help you securely authenticate and transport data on the [[Introduction to the internet|Internet]]. **Transport Layer Security** (*TSL*) and **Secure Socket Layers** (*SSL*) are cryptographic protocols that [[Encryption|encrypt]] data and authenticate a connection. 
Actually **TLS** is just a more recent version of **SSL**, which fixes some more vulnerabilities in the **SSL** protocols.
Here’s the full history of **SSL** and **TLS** releases:
- SSL 1.0 – never publicly released due to security issues.
- SSL 2.0 – released in 1995. Deprecated in 2011. Has known security issues.
- SSL 3.0 – released in 1996. Deprecated in 2015. Has known security issues.
- TLS 1.0 – released in 1999 as an upgrade to SSL 3.0. Planned deprecation in 2020.
- TLS 1.1 – released in 2006. Planned deprecation in 2020.
- TLS 1.2 – released in 2008.
- TLS 1.3 – released in 2018.


---


## How do TLS and SSL work to secure data?

When you install an SSL/TSL certificate on your web server, it includes a public key and a private key that authenticate your server and let your server encrypt and decrypt data. When a visitor goes to your site, their [[Browsers|web browser]] will look for your sites SSL/TSL certificate. Then, the [[Browsers|browser]] will perform a "handshake" to check the validity of your certificate and authenticate your server. If the SSL certificate is not valid, the users may be faced with the "your connection is not private" error, which could cause them to leave your website.

Once a visitor’s [[Browsers|browser]] determines that your certificate is valid and authenticates your server, it essentially creates an [[Encryption|encrypted]] link between it and your server to securely transport data.

This is also where [[HTTPS]] comes in ([[HTTPS]] stands for “[[HTTP]] *over SSL/TLS*”).

[[HTTP]], and the HTTP/2 are application protocols that play an essential role in transferring information over the [[Introduction to the internet|Internet]].

With plain [[HTTP]], that information is vulnerable to attack. But when you use [[HTTPS|HTTP over SSL/TLS]], you [[Encryption|encrypt]] and authenticate that data during transport, which makes it secure.

This is why you can safely process credit card details over [[HTTPS]] but **not** over [[HTTP]], and also why **Google Chrome** is pushing so hard for [[HTTPS]] adoption.



###### External Links:
---
[TLS vs SSL](https://kinsta.com/knowledgebase/tls-vs-ssl/)
[SSL und TSL](https://www.heise.de/tipps-tricks/SSL-und-TLS-was-ist-der-Unterschied-4884686.html)

---
