---
title: Java Duration作用
date: 2023-09-18 14:34:00
tags: 
	- Java
categories: Java
cover: https://i.loli.net/2020/03/30/PVp2TgjSiMDhv7F.jpg
---

在Java中，`Duration`是`java.time`包中的一个类，用于表示时间间隔的持续时间。它通常用于处理时间的差异，例如计算两个日期时间之间的时间差，或者执行时间的持续跟踪。

以下是一些`Duration`的常见用途：

1. 计算时间差：您可以使用`Duration`来计算两个`Instant`、`LocalDateTime`或其他日期时间对象之间的时间差。例如，您可以计算两个时间点之间的秒数、毫秒数等。

```java
Instant start = Instant.now();
// Some time-consuming operation
Instant end = Instant.now();
Duration duration = Duration.between(start, end);
long seconds = duration.getSeconds();
```

2. 执行时间测量：您可以使用`Duration`来测量代码块的执行时间。这对于性能优化和分析非常有用。

```java
Instant startTime = Instant.now();
// Code block to measure
Instant endTime = Instant.now();
Duration executionTime = Duration.between(startTime, endTime);
```

3. 时间单位转换：`Duration`允许您将时间间隔从一种单位转换为另一种单位，例如从秒到分钟、小时或天。

```java
Duration duration = Duration.ofSeconds(120);
long minutes = duration.toMinutes();
```

4. 操作时间间隔：您可以对`Duration`执行一些算术操作，如加法、减法和乘法，以便在时间间隔上执行各种操作。

```java
Duration duration1 = Duration.ofHours(2);
Duration duration2 = Duration.ofMinutes(30);
Duration sum = duration1.plus(duration2);
Duration difference = duration1.minus(duration2);
Duration multiplied = duration1.multipliedBy(3);
```

5. 格式化输出：您可以将`Duration`格式化为字符串以便于显示。

```java
Duration duration = Duration.ofMinutes(90);
String formattedDuration = duration.toString(); // "PT1H30M"
```

`Duration`是Java 8引入的日期时间API的一部分，使日期和时间的处理更加灵活和方便。它通常与`Instant`、`LocalDateTime`等其他日期时间类一起使用，以进行时间相关的计算和操作。

