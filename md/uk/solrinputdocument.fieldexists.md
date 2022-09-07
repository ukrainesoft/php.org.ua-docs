---
navigation:
  - solrinputdocument.destruct.md: '« SolrInputDocument::destruct'
  - solrinputdocument.getboost.md: 'SolrInputDocument::getBoost »'
  - index.md: PHP Manual
  - class.solrinputdocument.md: SolrInputDocument
title: 'SolrInputDocument::fieldExists'
---
# SolrInputDocument::fieldExists

(PECL solr> = 0.9.2)

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

Повертає **`true`** у разі, якщо поле знайдено та **`false`**, якщо ні.
