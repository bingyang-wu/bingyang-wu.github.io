---
title: Java设置SetCookie属性
date: 2020-10-23 22:45:00
tags: 
  - cookie
  - Java
categories: Java
---


### 在Controller层里加上

```java
    /**
     * 设置HttpOnly=true,SameSite=secure,Secure=true
     */
    @ModelAttribute
    public void setReqAndRes(HttpServletRequest request, HttpServletResponse response){
        response.setHeader("Set-Cookie", response.getHeader("Set-Cookie")+";SameSite=strict;HttpOnly;Secure=true");
    }
```