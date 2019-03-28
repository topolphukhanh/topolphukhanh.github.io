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

![Cassandra](https://lh3.googleusercontent.com/BPFJAvizVAtug6PIThh2AEpIWdNXpiqUaZ3388fU37SzrjGAu9nGSNmC0sl5DAhPPhpBl56KY3XPFGvWHPEkciZXFXeI7QinYSPtz3vqN7jFsNWyAvqx3UPkE5jlTPR3jYlDxWBVgnM6UivPfJ1a1aoi0_15L_mCUFJJnYFUHoYTDFh1QM8WImH8IBtV8g5A4GmmcLx_ylTu_Gu3CXzk7TqyM_qysTnLA0QPrX14Mt7UJO3p0MKBs1Xg4Yhu0zcHv7B4GvO9km8EothG7afeUOMknPDCuaiEOYASUGRYApEF20xFSIDxCE9i5qhlqw4OVAEYygcp8GCQ1eRb3m5y9BcoaA1Go2Z9OCmXvZIeUvCA1rzjqzaqwt9xVX4wrsnCv2WpHoeBj6_aq1qcsTZBASizzDh7fcZkOoQPRdldcHPRT8WwAvYkwPo04z8rmwyw-idLFDVxF4y_mghjf4x2IgzkXA9nERryCGBGXWZZSQgWOyWJ7JSZCdw8eLs7sw7cuXSmft1tko9LmLSX-f4WfNCauI-pMnutVlKwQDRMeqWOTk_J6XEcus3dJjNAjHOteGyEzC58YUj0qpsw-YLtJCrhDNBPb6TycUxpOJ6U9hzfPeIIktjzgFOfAGeQRWgcct4uEoZiMI-8UEUrOUi3CIVFFW-N8iM=w395-h278-no)

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
