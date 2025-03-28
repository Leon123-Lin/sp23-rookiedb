# CS 186: Introduction to Database Systems

## Overview:

> This is an intro database system(Spring 2023 version) course from UC Berkeley that I self learned in my personal time.
> Throughout this course, I read through all the notes on the course website and implemented 4 different components to support the functions of the Rookie Database. 

## Projects(spec):

- Project 2: [B+ Trees](https://cs186.gitbook.io/project/assignments/proj2)
- Project 3: [Joins and Query Optimization](https://cs186.gitbook.io/project/assignments/proj3)
- Project 4: [Concurrency](https://cs186.gitbook.io/project/assignments/proj4)
- Project 5: [Recovery](https://cs186.gitbook.io/project/assignments/proj5)

## Project Overview:

### B+ Trees:

In the B+ Trees project, I implemented the following methods:

> - <span style="color: green">get()</span>: return the corresponding leafnode of the B+ tree with the given key.
> - <span style="color: green">getLeftMostLeaf()</span>: return the left most leafnode of the B+ tree.
> - <span style="color: green">put()</span>: add a new key-record pair to the B+ tree.
> - <span style="color: green">remove()</span>: remove an exist key-record pair from the B+ tree.
> - <span style="color: green">bulkLoad()</span>: load pairs of the key-record pair into a B+ tree with a given load factor(<= 1.0).

in [LeafNode.java](https://github.com/Leon123-Lin/sp23-rookiedb/blob/main/src/main/java/edu/berkeley/cs186/database/index/LeafNode.java), 
[InnerNode.java](https://github.com/Leon123-Lin/sp23-rookiedb/blob/main/src/main/java/edu/berkeley/cs186/database/index/InnerNode.java) 
and [BPlusTree.java](https://github.com/Leon123-Lin/sp23-rookiedb/blob/main/src/main/java/edu/berkeley/cs186/database/index/BPlusTree.java).


### Joins and Query Optimization:

In the Joins and Query Optimization project, I implemented different join algorithms to join the tables and algorithm to form an optimal query plan.

> - [BNLJOperator.java](https://github.com/Leon123-Lin/sp23-rookiedb/blob/main/src/main/java/edu/berkeley/cs186/database/query/join/BNLJOperator.java): The block nested loop join algorithm.
> - [SortMergeOperator.java](https://github.com/Leon123-Lin/sp23-rookiedb/blob/main/src/main/java/edu/berkeley/cs186/database/query/join/SortMergeOperator.java): The sort merge join algorithm.
> - [QueryPlan.java](https://github.com/Leon123-Lin/sp23-rookiedb/blob/main/src/main/java/edu/berkeley/cs186/database/query/QueryPlan.java): Optimal plan selection algorithm.


### Concurrency:

In the Concurrency project, I implement a manager system to process the lock requests from different transactions.

> - [LockType.java](https://github.com/Leon123-Lin/sp23-rookiedb/blob/main/src/main/java/edu/berkeley/cs186/database/concurrency/LockType.java): Check whether two lock types are compatible, can be a parent and substitutable.
> - [LockManager.java](https://github.com/Leon123-Lin/sp23-rookiedb/blob/main/src/main/java/edu/berkeley/cs186/database/concurrency/LockManager.java): A manager system that keep track of the lock request and will decide whether add a lock request to the queue or process it.


### Recovery:

In the Recovery project, I implement a Aries Recover manager system to keep track of the log records and recover the database when it is crashed.

> - [ARIESRecoveryManager.java](https://github.com/Leon123-Lin/sp23-rookiedb/blob/main/src/main/java/edu/berkeley/cs186/database/recovery/ARIESRecoveryManager.java): A manager system that keep track of the log records and recover the database when it is necessary.
