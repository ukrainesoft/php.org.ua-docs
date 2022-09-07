---
navigation:
  - solrdocument.destruct.md: '« SolrDocument::destruct'
  - solrdocument.get.md: 'SolrDocument::get »'
  - index.md: PHP Manual
  - class.solrdocument.md: SolrDocument
title: 'SolrDocument::fieldExists'
---
# SolrDocument::fieldExists

(PECL solr> = 0.9.2)

SolrDocument::fieldExists — Перевіряє, чи існує поле в документі

### Опис

```methodsynopsis
public SolrDocument::fieldExists(string $fieldName): bool
```

Перевіряє, чи поле поле в документі є коректним ім'ям поля.

### Список параметрів

`fieldName`

Назва поля

### Значення, що повертаються

Повертає **`true`** якщо поле є і **`false`** якщо це не так.
