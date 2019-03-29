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

![Cassandra](https://lh3.googleusercontent.com/bl4AEWOd8m_6sUczuaHRRg2OB7DLR9wRskrUEwWAIanQjrNx6KhQ3ugcorJrn5BEWpzcAd0jabpa6I_TNx5VB482j0WFRmWB_uKV09NYsBBNuMHZUpA86AnB-rnZqGEnOmHUxnFABFPA3XFcpqz5PLKabR3leDHhHWUnGympXiKt-851dbvoiPSg1AToFIwaIxQVq8ks4L-Sc5XHPndcSiDL_e2dSNiKFBM8OFqAC8pZjZZfvzSlJqaGH8Gxrx4ikOx-VIRfZa25fqYkXy-6aCmLTx38qRL7zkLLCeNwPTGAWov1Vv4gggzNSHyQWUaxGXgFBzhwQJBU57_5WNEXynr3Tssn47NGcxKyX6hZJxBNsN_zWI8FfTdx56IwIt7NlP4pVfKj7SKniBtKbpoJoGIrzDOMWn-FGADQmht1myo-Oyj04dJjPMAU7-x3P4lBhNVePkyuKKndSdCX-EKWjnx6MpyT7iakAmQCI7fl0BDWP0ivRKkci2Pz5Yu1mr_dCWszkDKHPOfaQ9yeZ3EKqhU83D006bdjNwALoKY45znoAJOFWZfT2d7p4G0Wu-tReezVYL-E-C-h19pTjhyRGYkAg20CYPy_I-eTqp1Q5xnjUuXeRGoyIiAq3lNz4TPhV-lVA-kP63ozr4G42vdkWSdnLnDdzXk=w395-h278-no)

We have a strange query deploying, it takes 60 seconds to complete the query. Otherwise, it only take 0.16 seconds (mean) to complete query. 
Is timeout of cassandra? So what is the reason.

Follow the path of jobs query:
- It's cluster cassandra. networks trouble !? 
- memory !?, cassandra in memory trouble!? trouble with swap ram!? cassandra note recommend the swap space to run in product!?
- bad disk !?
- cpu resource trouble !?
- and what else!?


Reference:
1. [Swap space recommendation from redhat](https://access.redhat.com/documentation/en-us/red_hat_enterprise_linux/7/html/storage_administration_guide/ch-swapspace)
