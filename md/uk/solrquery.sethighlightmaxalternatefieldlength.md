---
navigation:
  - solrquery.sethighlighthighlightmultiterm.md: '« SolrQuery::setHighlightHighlightMultiTerm'
  - solrquery.sethighlightmaxanalyzedchars.md: 'SolrQuery::setHighlightMaxAnalyzedChars »'
  - index.md: PHP Manual
  - class.solrquery.md: SolrQuery
title: 'SolrQuery::setHighlightMaxAlternateFieldLength'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# SolrQuery::setHighlightMaxAlternateFieldLength

(PECL solr >= 0.9.2)

SolrQuery::setHighlightMaxAlternateFieldLength — Встановлює максимальну кількість символів поля для повернення

### Опис

```methodsynopsis
public SolrQuery::setHighlightMaxAlternateFieldLength(int $fieldLength, string $field_override = ?): SolrQuery
```

Якщо SolrQuery::setHighlightAlternateField() було передано значення **`true`**, цей параметр вказує максимальну кількість символів поля для повернення

Будь-яке значення менше або 0 означає необмежене.

### Список параметрів

`fieldLength`

Довжина поля

`field_override`

Ім'я поля

### Значення, що повертаються

Повертає поточний об'єкт SolrQuery, якщо використовується значення, що повертається.
