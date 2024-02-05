---
navigation:
  - solrquery.sethighlightalternatefield.md: '« SolrQuery::setHighlightAlternateField'
  - solrquery.sethighlightfragmenter.md: 'SolrQuery::setHighlightFragmenter »'
  - index.md: PHP Manual
  - class.solrquery.md: SolrQuery
title: 'SolrQuery::setHighlightFormatter'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# SolrQuery::setHighlightFormatter

(PECL solr >= 0.9.2)

SolrQuery::setHighlightFormatter — Задає засіб форматування для виведення виділення

### Опис

```methodsynopsis
public SolrQuery::setHighlightFormatter(string $formatter, string $field_override = ?): SolrQuery
```

Задає засіб форматування для виведення виділення

### Список параметрів

`formatter`

В даний час єдине допустиме значення - "simple"

`field_override`

Ім'я поля

### Значення, що повертаються

Повертає екземпляр [SolrQuery](class.solrquery.md)
