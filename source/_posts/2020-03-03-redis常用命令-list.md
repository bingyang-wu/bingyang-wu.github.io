---
title: redis常用命令-list
date: 2020-03-03 22:58:00
tags: redis
categories: redis
cover: https://i.loli.net/2020/03/04/ukGRnzUSA12Q8IW.png
---

# redis-list

## lpush

```code
lpush key value
```

放在链表的左边

## rpush

```code
rpush key value
```

放在链表的右边

## lrange

```code
lrange key start end
```

取链表中的元素 start:开始位置，end：结束位置，下标从0开始，含头含尾

start、end为负时从后往前数

lrange key 0 -1:获取所有元素

## lpop

```code
lpop key
```

从左边弹出值

## rpop

```code
rpop key
```

从右边弹出值

## lrem

```code
lrem key count value
```

从链表中删除count个值为value的

count为正时从头往尾删，负时从尾往头删

## ltrim

```code
ltrim key start end
```

只保留截取的部分

## lindex

```code
lindex key index
```

取下标为index的元素，下标从0开始

## llen

```code
llen key
```

查看链表长度

## linsert

```code
linsert key before|after pivot value
```

再某个数前|后插入数

## rpoplpush

```code
rpoplpush source destination
```

右边出，左边进，destination为右边出来的数

## brpop

## blpop

从右从左弹出，没有值时会等待直到有值时pop

## lset

```code
lset key index value
```

将下标为index的元素值改成value
