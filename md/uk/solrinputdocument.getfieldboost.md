---
navigation:
  - solrinputdocument.getfield.md: '« SolrInputDocument::getField'
  - solrinputdocument.getfieldcount.md: 'SolrInputDocument::getFieldCount »'
  - index.md: PHP Manual
  - class.solrinputdocument.md: SolrInputDocument
title: 'SolrInputDocument::getFieldBoost'
---
# SolrInputDocument::getFieldBoost

(PECL solr> = 0.9.2)

SolrInputDocument::getFieldBoost — Отримує значення підвищення для певного поля

### Опис

```methodsynopsis
public SolrInputDocument::getFieldBoost(string $fieldName): float
```

Отримує значення підвищення для певного поля.

### Список параметрів

`fieldName`

Назва поля.

### Значення, що повертаються

Повертає значення підвищення для поля або **`false`** у разі виникнення помилки.
