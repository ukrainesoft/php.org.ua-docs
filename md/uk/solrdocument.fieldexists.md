---
navigation:
  - solrdocument.destruct.md: '« SolrDocument::\_\_destruct'
  - solrdocument.get.md: 'SolrDocument::\_\_get »'
  - index.md: PHP Manual
  - class.solrdocument.md: SolrDocument
title: 'SolrDocument::fieldExists'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# SolrDocument::fieldExists

(PECL solr >= 0.9.2)

SolrDocument::fieldExists — Перевіряє, чи існує поле в документі

### Опис

```methodsynopsis
public SolrDocument::fieldExists(string $fieldName): bool
```

Перевіряє, чи є запитане поле коректним ім'ям поля у документі.

### Список параметрів

`fieldName`

Назва поля

### Значення, що повертаються

Повертає **`true`** якщо поле є і **`false`** якщо це не так.
