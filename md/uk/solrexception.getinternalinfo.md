---
navigation:
  - class.solrexception.html: « SolrException
  - class.solrclientexception.html: SolrClientException »
  - index.html: PHP Manual
  - class.solrexception.html: SolrException
title: 'SolrException::getInternalInfo'
---
# SolrException::getInternalInfo

(PECL solr> = 0.9.2)

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
