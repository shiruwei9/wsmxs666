# Project 3 – P2P System and Simulation
**COP5615 - Distributed Operating Systems Principles**

---
## Group Information

* [Shiru Wei- 08892233]
* [Jiaqi Cheng- lalalalala]

---

## What is working?  

#### Input

```F#
dotnet fsi .\Chord.fsx <nodeNum> <RequestNum>
```

#### Output

```F#
Running time, Global hop, Average hop
```

* The chord protocol is implemented using the APIs mentioned in section 4 of the paper [Chord: A Scalable Peer-to-peer Lookup Protocol] by Ion  Stoica,  Robert  Morris,  David  Karger and others and encode the application associating a key with a string. Our implementation works as expected, and we are able to change the message type and the specific activity with a simliar API(such as stablize, join) described in the paper.

* To avoid meeting collisions when we establish unique node ids, we do our approach with random number in the project.

* The maximum number of nodes we approach in the project is 1000 for the number of nodes and 100 for the number of request. In this process, we need to make sure that the number of mod (2^m) should be larger than the number of node

* The average hops is in the range of [3, 6] for our message to reach its destination with the number of nodes in the range of [50, 1000] and number of requests in the range of [20, 100]. 

* For the largest network we managed for testing(1000 for the number of nodes and 100 for the number of request), with an average over 10 times of running, the value of average hops is 5.3103. And it shows that the average lookup costs O(logN).

* For the largest network we managed for running, the number of nodes is more than 5000 and the number of request is more than 150
---

## Instructions(Bonus is included):

* The input provided (as command line to the program) will be of the form:

>$ mix run project3.exs numNodes numMessages
numNodes -> Required number of nodes to be set up in a chord  
numMessages -> Number of messages each node sends for lookups    
   
* The input for Bonus will be of the form:  
   
>$ mix run project3.exs numNodes numMessages numDeleteNodes   
numNodes -> Required number of nodes to be set up in a chord  
numMessages -> Number of messages each node sends for lookups  
numDeleteNodes -> Number of nodes to be deleted from the established nodes(failure model)   

---

## Result of running:

>$ *mix run project3.exs 1000 10   
Average hops for a message: 3.218
 ---
 
## Result of running(Bonus):

>$ *mix run project3.exs 1000 100 10   
Average hops for a message: 3.310  
 ---
