---
title: Demo
description: Welcome to Hugo Theme Stack
slug: hello-world
date: 2025-11-02 00:00:00+0000
image: cover2.jpg
categories:
    - Techincal Blog Category
tags:
    - Technical Tag
---

Trong một ngày đẹp trời, khi đang lướt Twitter để cập nhật tin tức và kĩ thuật thì mình va phải post alert về quả CVE critical của Sitecore, điểm CVSS tận 9.0. Với bản tính tò mò thì mình cũng đã bắt tay vào tìm hiểu và phân tích case critical này :D

![image.png](attachment:a3433665-5f5a-4e43-9a74-4d143815ca3f:image.png)

Trong bài có dẫn link blog của Google Mandiant phân tích về một đợt tấn công gần đây lên các instance Sitecore sử dụng sample machine key có trong các official deployment guides của Sitecore từ **tận năm 2017 và thậm chí là trước đó nữa**. 

![image.png](attachment:be2813d6-6e87-487a-b07a-5ab29fdb9baa:image.png)

Bài này có đề cập nguyên nhân gốc rễ lỗ hổng đến từ việc [ASP.NET](http://ASP.NET) machine key bị lộ dẫn đến attacker có thể kiểm soát cơ chế deserialize ViewState của các ứng dụng ASP.NET để khai thác RCE. Trước tiên, ta cần đi sâu và tìm hiểu xem cơ chế này diễn ra như thế nào.