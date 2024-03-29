# Project 3 – P2P System and Simulation
**COP5615 - Distributed Operating Systems Principles**

---
## Group Information

* [Shiru Wei- 08892233]
* [Jiaqi Cheng- 34563129]

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

![image](https://github.com/shiruwei9/wsmxs666/blob/master/Picture1.png)

* The chord protocol is implemented using the APIs mentioned in section 4 of the paper [Chord: A Scalable Peer-to-peer Lookup Protocol] by Ion  Stoica,  Robert  Morris,  David  Karger and others and encode the application associating a key with a string. Our implementation works as expected, and we are able to change the message type and the specific activity with a simliar API(such as stablize, join) described in the paper.

* To avoid meeting collisions when we establish unique node ids, we do our approach with random number in the project.

* The maximum number of nodes we approach in the project is 1000 for the number of nodes and 100 for the number of request. In this process, we need to make sure that the number of mod (2^m) should be larger than the number of node

* The average hops is in the range of [3, 6] for our message to reach its destination with the number of nodes in the range of [50, 1000] and number of requests in the range of [20, 100]. 

* For the largest network we managed for testing(1000 for the number of nodes and 100 for the number of request), with an average over 10 times of running, the value of average hops is 5.3103. And it shows that the average lookup costs O(logN).

* For the largest network we managed for running, the number of nodes is more than 5000 and the number of request is more than 150
---


