---
layout: post
title:  "System Design"
date:   2020-12-10 11:18:12 -0700
categories: system design
---

## Load-Balancing
* Goal: help developing a scalable app, allow distributing loads across servers based on metrics such as random, round-robin, random with weighting for memory or cpu utilization etc. 
    * Example: NGINX can proxy HTTP traffic to group servers

    ```
    # NGINX distributes requests among the servers in the group according to their weights using the Round Robin method. 
    http {
        upstream backend {
            server backend1.example.com weight=5;
            server backend2.example.com;
            server 192.0.0.1 backup;
        }
    }

    ```

* LB will stop sending requests server if the server is overloading, or not responding or has elevated error rate. 
* We typically add LBs in three places: 
    * b/t clients and web servers
    * b/t web servers and internal platform servers (e.g., application server, cache server etc)
    * b/t internal platform server and databases
* Ways to implement LB: normally start with a software LB, then move to client LB or hardware LB when needed. 
    * Software LB: e.g., HAPProxy: a LB and proxy server for TCP and HTTP-based applications that spreads requests across multiple servers. 
        * e.g., client uses a port `localhost:9000` to connect to the server. HAPProxy manages this port, every client request on this port will be received by the proxy and then passes to the backend service in an distributed way. **MORE INFO NEEDS TO BE FILLED IN FROM PROXIES**
    * Hardware LB: more expensive
    * Smart clients: detects hosts that are not responding and avoid sending more requests to them. e,g, add LB to database client


## Cache
* recently requested data is likely to be requested again. 

1. Application server cache
* 

Cache Eviction policies: 
1. First In First Out
2. Last in first out
3. least recently used
4. most recently used
5. least frequently used
6. random replacement: randomly selects a candidate and discard it to make space when necessary.