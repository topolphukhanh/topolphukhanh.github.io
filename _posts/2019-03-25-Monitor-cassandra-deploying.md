---
layout: post
title: Monitor performance cassandra for online algorithms
categories: [Architecture]
tags: [Architecture, Cassandra]
description: Monitor performance cassandra for sequence recommendation models
--- 

# Monitor performance cassandra for online algorithms

We using the cassandra to store sequence data from real-time streaming user logs, with deep learning algorithms deploying. 
The aim of solution is reaction to any event related the items. Performance of cassandra, especially speed of query must be required.

Some statistic description:

mean    |0.155917
std     |0.992435
min     |0.061545
25%     |0.092677
50%     |0.158961
75%     |0.176974
max     |60.189077


Monitor performance of Cassandra:

![Cassandra](https://lh3.googleusercontent.com/iYsHnlkKNi3jNnZkFP0tCe9juAAvzDTKaBh9mBwrrJxHVieCm2R_PF4iXrDoFeZBs3FpALvCPYaWdv28833Rb2C4XuUg1nfSYpvlLVMPOv6H7gXx7avPIf0W1YniCA8om93ThxIUSg=w395-h278-no)

We have a strange query deploying, it takes 60 seconds to complete the query. Otherwise, it only take 0.16 seconds (mean) to complete query. 
Is timeout of cassandra? So what is the reason.

Follow the path of jobs query:
- It's cluster cassandra. networks trouble !? 
- memory !?, cassandra in memory trouble!? trouble with swap ram!? cassandra does not recommend the swap space to run in product!?
- bad disk !?
- cpu resource trouble !?
- and what else!?


Reference:
1. [Swap space recommendation from redhat](https://access.redhat.com/documentation/en-us/red_hat_enterprise_linux/7/html/storage_administration_guide/ch-swapspace)
