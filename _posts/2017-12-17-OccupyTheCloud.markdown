---
layout: singleslide
title:  "论文介绍：Occupy the Cloud: Distrubted Computing for the 99%"
date:   2017-12-16 00:45:41 -0700
categories: "slide"
---

<style type="text/css">
.floatleft{float:left;width:40%;}
.floatright{float:right;width:60%;}
</style>


<textarea id="source">

class: center, middle

# Occupy the Cloud: Distrubted Computing for the 99%

&nbsp;
&nbsp;

##### Eric Jonas, Qifan Pu, Shivaram Venkataraman, Ion Stoica, Benjamin Recht
##### University of California, Berkeley
#### 2017-12-17



---

## Motivation

- In spite of many open source platforms and extensive commercial offerings, distributed computing remains inaccessible to a large number of users
    - Complex cluster management and configuration tools

- Cloud Computing can solve this problem to some extent, but the twin promises of **scale** and **elasticity** still remain out of reach for a large number of cloud computing users.

    - On commercial cloud platforms, a novice user confronts a dizzying array of potential decisions: one must ahead of time decide on instance type, cluster size, pricing model, programming model, and task granularity.
    - In fact, taking advantage of elasticity remains challenging for even sophisticated users, as the majority of these frameworks were designed to first target on-premise installations at large scale.
    - Such challenges are particularly surprising considering that the vast number of data analytic and scientific computing workloads remain embarrassingly parallel.

- **Serverless** execution model with **stateless** functions

    - simple,fundamentally elastic,user-friendly

---

## Is the cloud usable?
- Software configuration issues

    - The layers of abstraction present in distributed data processing platforms are complex and difficult to correctly configure.

    - For example, PySpark, arguably one of the easier to use platforms, runs on top of Spark (written in Scala) which interoperates and is closely coupled with HDFS (written in Java), Yarn (Java again), and the JVM. The JVM in turn is generally run on virtualized Linux servers. Merely negotiating the memory limit interplay between the JVM heap and the host operating system is an art form.

    - These systems often promote “ease of use” by showing powerful functionality with a few lines of code, but this ease of use means little without mastering the configuration of the layers below.

- Tremendous choice and workload management
    - AWS offers 70 instances types across 14 geographical datacenters

- Take advantage of dynamic market-based pricing of servers

    - Most of the above-mentioned frameworks make it difficult to handle machine preemption. To avoid the risk of losing intermediate data, users must be careful to either regularly checkpoint their data or run the master and a certain number of workers on non-spot instances.
---


## What users want?

Users simply wish they could easily “push a button” and have their code – existing, optimized, single-machine code – running on the cloud.


In an ideal world, users would simply be able to run their desired code across a large number of machines, bottlenecked only by serial performance. Executing 100 or 10000 five minute jobs should take roughly five minutes, with minimal start-up and tear-down overhead.

Need a simple abstraction that allows users to run arbitrary functions in the cloud without setting up and configuring servers/frameworks etc.

### Goal： allow as many users as possible to take existing, legacy code and run it in parallel, exploiting elasticity.


---

## A Modest Proposal

Problem: Designed for a server-oriented resource model

#### Use a serverless architecture with stateless functions as the unifying abstraction for data processing.

<img src="/slides/assets/images/arct.png" >

Users submit single-threaded functions to a global scheduler and while submitting the function they can also annotate the runtime dependencies required. Once the scheduler determines where a function is supposed to run, an appropriate container is created for the duration of execution.

Thus, in such a model all the inputs to functions and all output from functions need to be persisted on remote storage and we include client libraries to access both high-throughput and low latency shared storage systems.

---
## Generality for the rest of us ?

- Map + monolithic Reduce
- MapReduce
- Parameter Servers

### Discussion

- Resource balance
- Pricing
- Scalable Scheduling
- Distributed Storage
- Launch Overheads
---

class: center, middle

# 谢谢

</textarea>
