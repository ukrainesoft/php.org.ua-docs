---
navigation:
  - solrquery.gethighlightfields.md: '« SolrQuery::getHighlightFields'
  - solrquery.gethighlightfragmenter.md: 'SolrQuery::getHighlightFragmenter »'
  - index.md: PHP Manual
  - class.solrquery.md: SolrQuery
title: 'SolrQuery::getHighlightFormatter'
---
# SolrQuery::getHighlightFormatter

(PECL solr> = 0.9.2)

SolrQuery::getHighlightFormatter — Повертає засіб форматування для виділеного висновку

### Опис

```methodsynopsis
public SolrQuery::getHighlightFormatter(string $field_override = ?): string
```

Повертає засіб форматування для виділеного виводу

### Список параметрів

`field_override`

Ім'я поля

### Значення, що повертаються

Повертає рядок у разі успішного виконання та **`null`**, якщо значення не встановлено
