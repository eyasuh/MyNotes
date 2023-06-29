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