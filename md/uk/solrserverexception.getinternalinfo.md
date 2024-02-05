---
navigation:
  - class.solrserverexception.md: « SolrServerException
  - class.solrillegalargumentexception.md: SolrIllegalArgumentException »
  - index.md: PHP Manual
  - class.solrserverexception.md: SolrServerException
title: 'SolrServerException::getInternalInfo'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# SolrServerException::getInternalInfo

(PECL solr >= 1.1.0, >=2.0.0)

SolrServerException::getInternalInfo — Повертає внутрішню інформацію про те, де було викинуто виняток

### Опис

```methodsynopsis
public SolrServerException::getInternalInfo(): array
```

Повертає внутрішню інформацію про те, де було викинуто виняток.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає масив, що містить інформацію про те, де було викинуто виняток. Використовується лише розробниками модулів для налагодження.
