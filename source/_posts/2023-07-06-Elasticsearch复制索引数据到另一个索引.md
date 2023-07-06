---
title: Elasticsearch复制索引数据到另一个索引
date: 2023-07-06 13:44:00
tags: 
	- Elasticsearch
categories: Elasticsearch
cover: https://i.loli.net/2020/03/30/PVp2TgjSiMDhv7F.jpg
---


```shell
POST _reindex
{
  "source": {
    "index": "旧索引名称"
  },
  "dest": {
    "index": "新索引名称"
  }
}
```

可用于索引重建，数据迁移等场景