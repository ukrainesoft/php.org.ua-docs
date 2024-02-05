---
navigation:
  - class.solrexception.md: « SolrException
  - class.solrclientexception.md: SolrClientException »
  - index.md: PHP Manual
  - class.solrexception.md: SolrException
title: 'SolrException::getInternalInfo'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# SolrException::getInternalInfo

(PECL solr >= 0.9.2)

SolrException::getInternalInfo — Повертає внутрішню інформацію про те, де було викинуто виняток

### Опис

```methodsynopsis
public SolrException::getInternalInfo(): array
```

Повертає внутрішню інформацію про те, де було викинуто виняток.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає масив, що містить внутрішню інформацію про те, де була викликана помилка. Використовується лише для налагодження розробниками модулів.
