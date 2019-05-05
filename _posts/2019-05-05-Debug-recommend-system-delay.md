---
layout: post
title: A Recommender System for Debugging - Delay.
categories: [Architecture]
tags: [Architecture, Debug, System]
description: A Recommender System for Debugging - Delay.
--- 
# A Recommender System for Debugging - Delay.

Hệ thống recommendation system bị delay vài phút !?

Nguyên nhân là gì

Mindset sẽ là lần ngược các vết có khả năng:
- Bắt đầu từ hệ thống
- Quá trình logs trễ
- Quá trình tương tác với logs


Tôi bắt đầu từ các function của hệ thống trước, với logger:
- Data processing, generate features, mapping, tương tác với các database metadata
- Models 
- Computing GPU
- Computing CPU/RAM
- Data processing save result prediction
- Database/Cache tương tác với API
Kết quả monitor những vấn đề này hoạt động bình thường.

Quá trình ghi logs (Message queue, Sparking streaming resource, Cassandra lưu hành vi người dùng) hoạt động bình thường.

Quá trình ghi recieve_at trên logs hoạt động bình thường về thời gian. Tuy nhiên có một server có thời gian chậm hơn giờ đúng. Serve này có function sử lý processing data, ảnh hưởng đến quá trình processing data.

![Time](/pictures/Time_server_Screeshotfrom2019-05-0510-21-14.png)

Update lại time cho server này. Thứ 2 lên thảo luận với anh em.

Reference:
[Microsoft - A Recommender System for Debugging](https://www.microsoft.com/en-us/research/wp-content/uploads/2016/02/esec099-ashok.pdf)