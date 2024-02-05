---
navigation:
  - class.solrclientexception.md: « SolrClientException
  - class.solrserverexception.md: SolrServerException »
  - index.md: PHP Manual
  - class.solrclientexception.md: SolrClientException
title: 'SolrClientException::getInternalInfo'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# SolrClientException::getInternalInfo

(PECL solr >= 0.9.2)

SolrClientException::getInternalInfo — Повертає внутрішню інформацію про те, де було викинуто виняток

### Опис

```methodsynopsis
public SolrClientException::getInternalInfo(): array
```

Повертає внутрішню інформацію про те, де було викинуто виняток.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає масив, що містить внутрішню інформацію про те, де була викликана помилка. Використовується лише для налагодження розробниками модулів.
