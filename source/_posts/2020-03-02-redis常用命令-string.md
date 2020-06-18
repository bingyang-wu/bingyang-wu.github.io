---
title: redis常用命令-string
date: 2020-03-02 21:14:00
tags: redis
categories: redis
cover: https://i.loli.net/2020/03/04/ukGRnzUSA12Q8IW.png
---

# redis常用命令-string

## set

```code
set key value ex | px  nx|xx
```

* ex: 秒 set a 1 ex 10,		10秒有效

* px: 毫秒 set a1 ex 10,      10毫秒有效
* nx：key不存在时执行操作
* xx:   key存在时执行操作

## mset

一次设置多个值 mset a  1 b 2 c 3 d 4

## mget

一次获取多个值 mget a b c d

## setrange

setrange  key offset  value

set a hello

setrange a 2 ??

结果: he??o

## append 

附加 append a 123

## getrange 

getrange key start end,含头含尾

## getset

获取到旧值并设置新值 getset a 123

## incr

加1，incr a，

incrby a 10,a加10

incrbyfloat a 10.5,浮点数增加

## decr

减1，

decrby  a 10,a减10

decrbyfloat a 10.5,浮点数减

## setbit

位运算:setbit key offset value

setbite char 2 1, 将第二位设置为1 +32，将大写字符改为小写字符。

offset:最大2^32-1,一个字符占8个位，2^（32-3），512M,一个字符串最大所占空间。

## bitop

bitop operation destkey  [key]

bitop or des key1 key2 key3: 将key1、key2、key3做or操作，结果放入des

operation:and、or、not、xor

