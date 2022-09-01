---
navigation:
  - solrinputdocument.setboost.html: '« SolrInputDocument::setBoost'
  - solrinputdocument.sort.html: 'SolrInputDocument::sort »'
  - index.html: PHP Manual
  - class.solrinputdocument.html: SolrInputDocument
title: 'SolrInputDocument::setFieldBoost'
---
# SolrInputDocument::setFieldBoost

(PECL solr> = 0.9.2)

SolrInputDocument::setFieldBoost — Встановлює значення підвищення індексу часу для поля

### Опис

```methodsynopsis
public SolrInputDocument::setFieldBoost(string $fieldName, float $fieldBoostValue): bool
```

Встановлює значення індексу часу для поля. Замінює поточне значення для цього поля.

### Список параметрів

`fieldName`

Назва поля.

`fieldBoostValue`

Індекс часу для підвищення значення.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.
