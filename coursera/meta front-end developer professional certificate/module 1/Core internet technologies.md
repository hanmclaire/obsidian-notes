---
title: Core internet technologies
date: 2025-02-02
---
==Introduction to Internet Protocols==
- There is a surprising parallel between the postal system and how the computer sends and receives data across the internet every day.
- Data sent across the internet is quite an important part of our everyday lives and it wouldn't be possible without **Internet Protocol addresses** or *IP addresses*. A useful way to think of IP addresses is that they function much like addresses in a postal system.
- Every computer on a network is assigned an IP address. In protocol version four an IP address contains four octet. It's separated by periods or dots. For example 192.0.2.235.
- When you send data across a network, you send the data as a series of messages called *IP packets*. Also known as *data grams* at a high level IP packets contain a header and a payload or the data. 
	- Like real mail, IP packets include the destination IP address and source IP address. These addresses are in the header along with some additional information to help deliver the packet. And the payload contains the data of the packet and some of the other protocols.
	- Like real mail issues, IP packets too they can arrive out of order, become damaged or corrupted to in transit or be dropped or lost during transit. To solve these problems, the payload part of the packets contains other protocols too.
- The two most common protocols are the Transmission Control Protocol referred to as TCP and the User Datagram Protocol, also known as UDP. 
	- *TCP* can solve all three of the previously mentioned issues but at the cost of a small delay when sending the data. This protocol is used for sending the data that must arrive correctly and in order such as a text or image files. 
	- *UDP* solves the corrupt packet issue but packets can still arrive out of order or not arrive at all. This protocol is used for sending data that can tolerate some data loss such as voice calls or live video streaming.
	- Both of these protocols contain payloads that contain further protocols inside of them and there you have it.
- These protocols can help to make sure that data arrives in order does not become corrupted or lost or dropped during transit.

==Introduction to HTTP==
- HTTPS is the secure version of HTTP.
- *HTTP*, which for Hypertext Transfer Protocol, is a core operational protocol of the world wide web. It is what enables your web browser to communicate with a web server that hosts a website.
- HTTP is the communication protocol that is request response based which you use whenever you browse the web. It is a protocol used for transferring web resources such as HTML documents, images, styles, and other files.
- A web browser or client sends an HTTP request to a server and the web server sends the HTTP response back to the browser.
- An HTTP requests consists of a method, path, version and headers. 
- The HTTP method describes the type of action that the client must performed.
	- The primary or the most commonly used HTTP methods are, GET, POST, PUT, and DELETE. 
	- The GET method is used to retrieve information from the given server.
	- The POST request is used to send data to the server.
	- The PUT method updates whatever currently exists on the web server with something else.
	- The DELETE method removes the resource.
- The path is the representation of where the resource is stored on the web server.
- 

| Additional Resources |
| -------------------- |
|                      |

