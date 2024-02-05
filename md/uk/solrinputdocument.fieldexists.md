---
navigation:
  - solrinputdocument.destruct.md: '« SolrInputDocument::\_\_destruct'
  - solrinputdocument.getboost.md: 'SolrInputDocument::getBoost »'
  - index.md: PHP Manual
  - class.solrinputdocument.md: SolrInputDocument
title: 'SolrInputDocument::fieldExists'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# SolrInputDocument::fieldExists

(PECL solr >= 0.9.2)

SolrInputDocument::fieldExists — Перевіряє, чи існує поле

### Опис

```methodsynopsis
public SolrInputDocument::fieldExists(string $fieldName): bool
```

Перевіряє, чи існує поле

### Список параметрів

`fieldName`

Назва поля.

### Значення, що повертаються

Повертає **`true`**в случае, если поле найдено и**`false`**, якщо ні.
