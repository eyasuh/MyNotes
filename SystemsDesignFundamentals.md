# Systems Design Fundamentals

## Table of Contents

- [Introduction](#introduction)
- [Key Concepts](#key-concepts)
- [System Architecture](#System-Architecture)
- [Usage](#usage)
## Introduction

This note covers the basics and condensed part of systems design fundamentals. Systems design takes multi solution approach and thus there is no single right approach.  

## Client-Server Model

 > **Client <---------> Server**
>> **Client:** the machine/process that requests data/info from a server  
>> **Server:** the process that responds to request from clients using network calls.  
>> **IP address:** address given to each machine consisting of four numbers (0-255) separated by dots. Try - on unix systems terminals `dig google.com` returns DNS queries.  
- 127.0.0.1 points to localhost
- 192.168.x.y private network
>> **DNS:** Domain Name System, contains information about a specific IP address(ex. phone contact lists contain names: number pair).
>> **Port:** Numbers that alow access from multiple points from the same IP address(think of phone numbers and extension numbers, the extension number would be the port).

**Common ports:** 
- 22: secure shell
- 53: DNS lookup
- 80: HTTP
- 443: HTTPS

## Network Protocols

Network protocol is a rule for communications between two or more machines consisting of types, format, order, and responses of massages.

**IP:**  Internet Protocol. Made of IP packets.
**Packet:** contains two main sections. 
 1. Header: contains info about packet(source, destination, size, version of IPs) 
 2. Data: contains the info to be sent(ie. the body)

**TCP** alow ordered delivery of packets.

**HTTP** an implementation of request/response paradigm. 

*Requests:* typically contain
```
    host: String (googl.com)
    port: integer (80 or 443)
    method: String (GET, PUT, POST, DELETE...)
    path: path (/home)
    headers: pair list ("content type": "application/json")
    body: sequence of bytes
```
*Response:* contains 
```
    status code: integer (200)
    headers: pair list 
    body: bytes
```

## Proxies

**Forward Proxy:** A server that is between the client and server. It acts on behalf of the client serving as the facilitator.  

**Reverse proxy:** A server that is between the server and client acting on behalf of the server. (Nginx)

Some use cases of Reverse Proxy:
- Filtering out requests
- Taking care of logging
- Caching
- Load balancing (distributing loads on different servers)
