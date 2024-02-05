---
navigation:
  - solrinputdocument.setboost.md: '« SolrInputDocument::setBoost'
  - solrinputdocument.sort.md: 'SolrInputDocument::sort »'
  - index.md: PHP Manual
  - class.solrinputdocument.md: SolrInputDocument
title: 'SolrInputDocument::setFieldBoost'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# SolrInputDocument::setFieldBoost

(PECL solr >= 0.9.2)

SolrInputDocument::setFieldBoost — Встановлює значення підвищення індексу часу для поля

### Опис

```methodsynopsis
public SolrInputDocument::setFieldBoost(string $fieldName, float $fieldBoostValue): bool
```

Встановлює значення індексу часу поля. Замінює поточне значення для цього поля.

### Список параметрів

`fieldName`

Назва поля.

`fieldBoostValue`

Індекс часу для підвищення значення.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.
