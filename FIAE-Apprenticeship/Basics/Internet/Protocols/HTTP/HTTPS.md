# HTTPS
---


## What is HTTPS?

**Hypertext transfer protocol secure** (*HTTPS*) is the secure version of [[HTTP]], which is the primary protocol used to send data between a [[Browsers|web browser]] and a [[Hosting|website]]. **HTTPS** is [[Encryption|encrypted]] in order to increase security of data transfer. This is particularly important when users transmit sensitive data, such as by logging into a bank account, [[SMTP|email service]], or health insurance provider.

Any [[Hosting|website]], especially those that require login credentials, should use **HTTPS**. In modern [[Browsers|web browsers]] such as *Chrome*, websites that do not use **HTTPS** are marked differently than those that are. Look for a padlock in the [[Domain Names#Whats the difference between a domain name and a URL?|URL]] bar to signify the webpage is secure. Web browsers take **HTTPS** seriously; *Google Chrome* and other [[browsers]] flag all **non-HTTPS** websites as not secure. 


---


## How does HTTPS work?

**HTTPS** uses an [[Encryption|encryption]] protocol to encrypt communications. The protocol is called [[SSL-TSL|TLS]], although formerly it was known as [[SSL-TSL|SSL]]. This protocol secures communications by using whats known as an asymmetric public key infrastructure. This type of security system uses two different keys to [[Encryption|encrypt]] communications between two parties:
1. **The private key**: this key is controlled by the owner of a website and it’s kept, as the reader may have speculated, **private**. This key lives on a web server and is used to decrypt information encrypted by the public key.
2. **The public key**: this key is available to everyone who wants to interact with the server in a way that’s secure. Information that’s encrypted by the public key can only be decrypted by the private key.


---


## Why is HTTPS important? What happens if a website doesn't have HTTPS?

**HTTPS** prevents websites from having their information broadcast in a way that’s easily viewed by anyone snooping on the [[Network]]. When information is sent over regular **HTTP**, the information is broken into packets of data that can be easily “sniffed” using free software. This makes communication over the an unsecure medium, such as *public Wi-Fi*, highly vulnerable to interception. In fact, all communications that occur over [[HTTP]] occur in plain text, making them highly accessible to anyone with the correct tools, and vulnerable to *on-path-attacks*.

With **HTTPS**, traffic is encrypted such that even if the packets are sniffed or otherwise intercepted, they will come across as nonsensical characters. Let’s look at an example:

### Before encryption:

>This is a string of text that is completely readable

### After encryption:

>ITM0IRyiEhVpa6VnKyExMiEgNveroyWBPlgGyfkflYjDaaFf/Kn3bo3OfghBPDWo6AfSHlNtL8N7ITEwIXc1gU5X73xMsJormzzXlwOyrCs+9XCPk63Y+z0=


In websites without **HTTPS**, it is possible for [[ISP|Internet Service Providers]] (*ISPs*) or other intermediaries to inject content into webpages without the approval of the website owner. This commonly takes the form of advertising, where an *ISP* looking to increase revenue injects paid advertising into the webpages of their customers. Unsurprisingly, when this occurs, the profits for the advertisements and the quality control of those advertisements are in no way shared with the website owner. **HTTPS** eliminates the ability of unmoderated third parties to inject advertising into web content.


---


## What port does HTTPS use?

**HTTPS** uses [[Ports|port]] **443**. This differentiates **HTTPS** from [[HTTP]], which uses [[Ports|port]] **80**.

(In *networking*, a [[Ports|port]] is a virtual software-based point where [[network]] connections start and end. All network-connected computers expose a number of [[Ports|ports]] to enable them to receive traffic. Each [[Ports|port]] is associated with a specific process or service, and different protocols use different [[Ports|ports]].)




###### External Links:
---
[What is HTTPS?](https://www.cloudflare.com/learning/ssl/what-is-https/)

---
#TCP/IP #TCP #IP #Internet #Application-Layer #Communication-Layer #Ports #HTTPS #HTTP #SPDY #Multiplexing #Header-Compression #Server-Push #Request-Prioritization #Binary-Protocol #Frames-and-Streams #Pipelining #Three-way-handshake #SYN #SYN-ACK #ACK #Status-codes #Server-Header #RST-STREAM #PUSH-PROMISE #TLS #HPACK #Huffman-code #Encryption #URLs