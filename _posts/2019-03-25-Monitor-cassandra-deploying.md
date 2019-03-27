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

![Cassandra](https://lh3.googleusercontent.com/Z4I6lzGmk172GNDQVFTvXHshqoQ0YLs-vcD44Rwg92fpZcH4AsMzgZ2SpnJFUySs7ko831-l8pcTGo8cBUP-mA_dQ5bslxp3I3q4wlMxZ0BtrbMFKv7InAq5xKUiHApP8ZCptWcyvvA20_HH9-zNqJGrYFi4SJQJI5P3rqHx4jYwWD9c-gt1jvjvUunmjkN-UiOqOY3RsmlIvrfYVBOWgATLrSa9sVDhamkxuY_4Xscr_zBmqhydBOmf7i8pdtmsJQQV5fhSGbHkWCsa7V2J-r5uA9K59hoLFniw47IY2hc8EsbsVKg2H_e0US7-1gq9lOMwkozDSvPblSGEkfbxBALHVz4nd9HLQEB_GbCcDFcGJddM1_8iygRt9EUcHkLCL_QPzb_JTVwaKgCf3LtkmALfXNbBFG-n4qqmpAQEXzMZHS1oEZmhBXsk2VVP_4hNS_B33hSLNXhze0-cfeZYFRq15kwVGcMobMtAsWT8yw_hQWSLrv-9yQpsPa7AhocrM0T3YeOUZOvhdzk6zUqqB3S-H0H3dJ8W5dy_fs7h6aNk9n71V-6DcgHeaBu8f9NUPmL3juRx9CLwgknLukNNlUUml5gV2xnkhY1BTgKQVSWtw4AmHKccJC4ErZexycqklfLEpC0ZYc3ePByM2g4CkmZgWOY76II=w395-h278-no)

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
