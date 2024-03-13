# Introduction to the internet


---

## What is the internet?

A group of computers or other devices which are connected to each other form a [[Network]]. All [[Network|networks]] connected together form the internet.

> The internet is a [[network]] of [[network|networks]].

The United States Department of Defense developed the internet back in the late 60s as a means of creating a decentralized communication [[network]] that could withstand a nuclear attack. Since then it evolved into a complex and sophisticated [[network]] that spans the globe.

By now its unimaginable how our modern life could work without the internet, since almost everyone uses it to access information, communicate with friends and family, conduct business and so much more. 

>As a developer, it is essential to understand how the internet works and the various technologies and protocols that underpin it.


---

## How the Internet Works: An Overview

At a high level, the internet works by connecting devices and computer systems together using a set of standardized protocols. These protocols define how information is exchanged between devices and ensure that data is transmitted reliably and securely.

The core of the internet is a global network of interconnected [[Router|routers]], which are responsible for directing traffic between different devices and systems. When sending data over the internet, it gets broken up into smaller packets that are sent from your device to your [[Router|router]]. The [[Router|router]] examines the packet and forwards it to the next [[router]] in the path towards its destination. This process continues until the packet reaches its final destination.

To ensure that packets are sent and received correctly, the internet uses a variety of protocols, including the **Internet Protocol** ([[IP]]) and the **Transmission Control Protocol** ([[TCP]]). [[IP]] is responsible for routing packets to their correct destination, while [[TCP]] ensures that packets are transmitted reliably and in their correct order.

In Addition to these core protocols, there are a wide range of other technologies and protocols that are used to enable communication and data exchange over the internet, including the [[DNS|Domain Name System]], the [[HTTP|Hypertext Transfer Protocol]], and the [[SSL-TSL|Secure Sockets Layer/Transport Layer Security protocol]]. 

>As a developer, it is important to have a solid understanding of how these different technologies and protocols work together to enable communication and data exchange over the internet


---


## Introduction to HTTP and HTTPS

[[HTTP]] (*Hypertext Transfer Protocol*) and [[HTTPS]] (*HTTP Secure*) are two of the most commonly used protocols in internet-based applications and services.

[[HTTP]] is the protocol used to transfer data between a client (such as a web browser) and a server (such as a website). When you visit a website, your web browser sends an [[HTTP]] request to the server, asking for the webpage or other resource you’ve requested. The server then sends an [[HTTP]] response back to the client, containing the requested data.

[[HTTPS]] is a more secure version of [[HTTP]], which encrypts the data being transmitted between the client and server using [[SSL-TSL|SSL/TSL]] (*Secure Sockets Layer/Transport Layer Security*) [[Encryption]]. This provides an additional layer of security, helping to protect sensitive information such as login credentials, payment information, and other personal data.

When you visit a website that uses [[HTTPS]], your web [[Browsers|browser]] will display a padlock icon in the address bar, indicating that the connection is secure. You may also see the letters “*https*” at the beginning of the website address, rather than “*http*”.


---


## Building Applications with TCP/IP

[[TCP]]/[[IP]] (*Transmission Control Protocol/Internet Protocol*) is the underlying communication protocol used by most internet-based applications and services. It provides a reliable, ordered, and error-checked delivery of data between applications running on different devices.

When building applications with [[TCP]]/[[IP]], there are a few key concepts to understand:

- [[Ports]]: Ports are used to identify the application or service running on a device. Each application or service is assigned a unique port number, allowing data to be sent to the correct destination.
- **Sockets**: A socket is a combination of an [[IP]] address and a [[Ports|port]] number, representing a specific endpoint for communication. **Sockets** are used to establish connections between devices and transfer data between applications.
- **Connections**: A connection is established between two sockets when two devices want to communicate with each other. During the connection establishment process, the devices negotiate various parameters such as the maximum segment size and window size, which determine how data will be transmitted over the connection.
- **Data transfer**: Once a connection is established, data can be transferred between the applications running on each device. Data is typically transmitted in segments, with each segment containing a sequence number and other metadata to ensure reliable delivery.

When building applications with [[TCP]]/[[IP]], you’ll need to ensure that your application is designed to work with the appropriate [[ports]], **sockets**, and **connections**. You’ll also need to be familiar with the various protocols and standards that are commonly used with [[TCP]]/[[IP]], such as [[HTTP]], [[FTP]] (*File Transfer Protocol*), and [[SMTP]] (*Simple Mail Transfer Protocol*). Understanding these concepts and protocols is essential for building effective, scalable, and secure internet-based applications and services.

## Securing Internet Communication with [[SSL-TSL|SSL/TLS]]

As we discussed earlier, [[SSL-TSL|SSL/TLS]] is a protocol used to encrypt data being transmitted over the internet. It is commonly used to provide secure connections for applications such as [[Browsers|web browsers]], [[SMTP|email clients]], and [[FTP|file transfer programs]].

When using [[SSL-TSL|SSL/TLS]] to secure internet communication, there are a few key concepts to understand:

- **Certificates:** [[SSL-TSL|SSL/TLS]] certificates are used to establish trust between the client and server. They contain information about the identity of the server and are signed by a trusted third party (a Certificate Authority) to verify their authenticity.
    
- **Handshake:** During the [[SSL-TSL|SSL/TLS]] handshake process, the client and server exchange information to negotiate the encryption algorithm and other parameters for the secure connection.
    
- [[Encryption]]: Once the secure connection is established, data is encrypted using the agreed-upon algorithm and can be transmitted securely between the client and server.
    

When building internet-based applications and services, it’s important to understand how [[SSL-TSL|SSL/TLS]] works and to ensure that your application is designed to use [[SSL-TSL|SSL/TLS]] when transmitting sensitive data such as login credentials, payment information, and other personal data. You’ll also need to ensure that you obtain and maintain valid [[SSL-TSL|SSL/TLS]] certificates for your servers, and that you follow best practices for configuring and securing your [[SSL-TSL|SSL/TLS]] connections. By doing so, you can help protect your users’ data and ensure the integrity and confidentiality of your application’s communication over the internet.


---


## The Future: Emerging Trends and Technologies

>The internet is constantly evolving, and new technologies and trends are emerging all the time. As a developer, it’s important to stay up-to-date with the latest developments in order to build innovative and effective applications and services.

Here are some of the emerging trends and technologies that are shaping the future of the internet:

- **5G:** 5G is the latest generation of mobile network technology, offering faster speeds, lower latency, and greater capacity than previous generations. It is expected to enable new use cases and applications, such as autonomous vehicles and remote surgery.
    
- [[Internet of Things]] **(IoT):** *IoT* refers to the [[network]] of physical devices, vehicles, home appliances, and other objects that are connected to the internet and can exchange data. As *IoT* continues to grow, it is expected to revolutionize industries such as healthcare, transportation, and manufacturing.
    
- [[Artificial Intelligence]] **(AI):** *AI* technologies such as machine learning and natural language processing are already being used to power a wide range of applications and services, from voice assistants to fraud detection. As *AI* continues to advance, it is expected to enable new use cases and transform industries such as healthcare, finance, and education.
    
- [[Blockchain]]: Blockchain is a distributed ledger technology that enables secure, decentralized transactions. It is being used to power a wide range of applications, from cryptocurrency to supply chain management.
    
- [[Edge computing]]: Edge computing refers to the processing and storage of data at the edge of the [[network]], rather than in centralized data centers. It is expected to enable new use cases and applications, such as real-time analytics and low-latency applications.
    

By staying up-to-date with these and other emerging trends and technologies, you can ensure that your applications and services are built to take advantage of the latest capabilities and offer the best possible experience for your users.


---


## Conclusion


- The internet is a global [[network]] of interconnected computers that uses a standard set of communication protocols to exchange data.
- The internet works by connecting devices and computer systems together using standardized protocols, such as [[IP]] and [[TCP]].
- The core of the internet is a global [[network]] of interconnected [[Router|routers]] that direct traffic between different devices and systems.
- Basic concepts and terminology that you need to familiarize yourself with include packets, routers, IP addresses, domain names, [[DNS]], [[HTTP]], [[HTTPS]], and [[SSL-TSL|SSL/TLS]].
- Protocols play a critical role in enabling communication and data exchange over the internet, allowing devices and systems from different manufacturers and vendors to communicate seamlessly.



###### External Links:
---
[How does the Internet Work?](https://cs.fyi/guide/how-does-internet-work)
[The internet, explained](https://www.vox.com/2014/6/16/18076282/the-internet)
[How does the Internet Work? - Stanford](https://web.stanford.edu/class/msande91si/www-spr04/readings/week1/InternetWhitepaper.htm)
[How does the Internet Work? - Roadmap](https://roadmap.sh/guides/what-is-internet)

---

#Internet #Networks #IP #TCP #Router #Packets 