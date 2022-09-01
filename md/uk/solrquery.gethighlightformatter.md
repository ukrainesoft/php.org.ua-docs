---
navigation:
  - solrquery.gethighlightfields.html: '« SolrQuery::getHighlightFields'
  - solrquery.gethighlightfragmenter.html: 'SolrQuery::getHighlightFragmenter »'
  - index.html: PHP Manual
  - class.solrquery.html: SolrQuery
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
