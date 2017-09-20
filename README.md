# Building highly scalable applications : Hello world !


Common server architecture patterns for highly scalable applications

There is no one-size-fits-all solution to improving scalability and performance. 
Belowe are a number of patterns that occur frequently:

    #Divide and conquer: 
    Divide a problem into many smaller problems and solve the problems across many CPUs 
    or servers so that each one has to do less  work. Examples: multiple web servers, 
    replicating or sharding a database, MapReduce.
    
    Caching: 
    Do the work ahead of time and save your results so instead of computing them on-demand, 
    you just retrieve precomputed values from storage. Examples: database caches, 
    denormalized schemas, distributed caches, CDNs, cookies, memoization, dynamic programming algorithms.
    
    Laziness: 
    Avoid doing work by putting it off until it's absolutely necessary. 
    Examples: lazy-loading parts of a web page only when you scroll to it, optimistic locking in a database.
    Approximate correctness: In many cases, it takes less work to get an answer that is "close enough" 
    than to get one that's exactly correct. Examples: eventual consistency, HyperLogLog, 
    reduced durability guarantees, best-effort messaging.
    
    Asynchrony:
    Instead of locking or blocking while waiting on the result of a computation, continue to
    do work and have the computation notify you when it's done. 
    Examples: non-blocking I/O, event loops, lock-free data structures.
    Jitter and randomization: Avoid spikes and hot spots by trying to spread the load out evenly. 
    Examples: randomizing cache expiration dates, load-balancing algorithms (round robin, priority scheduling), 
    algorithms for key partitioning (e.g., range partitioning, hash partitioning).
    
    Throttling: 
    Reject certain computations so that they don't slow down other ones. 
    Examples: rate-limiting requests on a server or removing slow servers from the request path.
    
    Redundancy: 
    Kick off the same computation more than once and return the one that finishes fastest. 
    Examples: backup or hedged requests in distributed systems, redundant servers in case of failure
    (e.g., hot-standby for a database).
    
    Co-location: 
    Move things physically closer together to reduce latency. 
    Examples: CDNs, multiple data centers around the world, putting related servers in the same server rack.
    
    Faster hardware: 
    AKA vertical scaling. 
    Examples: faster CPU, more RAM, more CPU cache, solid-state hard drives, faster networks, 
    performing computations in RAM instead of on disk or in the CPU cache instead of in RAM.
    
