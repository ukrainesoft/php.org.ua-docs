---
navigation:
  - solrquery.sethighlightfragmenter.md: '« SolrQuery::setHighlightFragmenter'
  - solrquery.sethighlighthighlightmultiterm.md: 'SolrQuery::setHighlightHighlightMultiTerm »'
  - index.md: PHP Manual
  - class.solrquery.md: SolrQuery
title: 'SolrQuery::setHighlightFragsize'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# SolrQuery::setHighlightFragsize

(PECL solr >= 0.9.2)

SolrQuery::setHighlightFragsize — Розмір фрагментів, які слід враховувати при виділенні

### Опис

```methodsynopsis
public SolrQuery::setHighlightFragsize(int $size, string $field_override = ?): SolrQuery
```

Встановлює розмір символів фрагментів для виділення. "0" вказує на те, що слід використовувати всі значення поля (без фрагментації).

### Список параметрів

`size`

Розмір символів фрагментів, які слід враховувати при виділенні

`field_override`

Ім'я поля

### Значення, що повертаються

Повертає поточний об'єкт SolrQuery, якщо використовується значення, що повертається.
