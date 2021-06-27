---
layout: post
title:  "File Transfer Protocol"
date:   2020-12-10 11:18:12 -0700
categories: FTP, SFTP
---

## FTP (File Transfer Protocol)
* It is a client/server network protocol used to transfer files over the Internet. FTP clients are used to send and retrieve files to and from servers which store files and respond to requests from clients.

## SFTP (Secure File Transfer Protocol)
* It is a file transfer protocol that leverages a set of utilities that provide **secure access** to a remote computer to deliver secure communications.
* It leverages SSH (Secure Socket Shell or Secure Shell)
* Secure FTP also compresses all data during the transmission, which can result in faster file transfers.

## SCP (Secure Copy)
* can copy from your local system to a remote system, from a remote system to your local system, between two remote systems from your local system
* in WSL2, `scp <C:/Desktop/local file> an12344@wip12234.eng.xxx.ca:<folder to copy to>`

## FileZilla (Tool has GUI)
* set a `new Site`, and type in your `Host`, `Protocol(often use SFTP)`, enter Login `User` and `Password`. 

## Tool
* [Accellion](https://www.accellion.com/company/careers/)
    * We uses Accellion to safely transfer our software to CORA customers, sending it is like sending an email, except it is Accellion email.