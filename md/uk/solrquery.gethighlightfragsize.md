---
navigation:
  - solrquery.gethighlightfragmenter.md: '« SolrQuery::getHighlightFragmenter'
  - solrquery.gethighlighthighlightmultiterm.md: 'SolrQuery::getHighlightHighlightMultiTerm »'
  - index.md: PHP Manual
  - class.solrquery.md: SolrQuery
title: 'SolrQuery::getHighlightFragsize'
---
# SolrQuery::getHighlightFragsize

(PECL solr> = 0.9.2)

SolrQuery::getHighlightFragsize — Повертає кількість фрагментів символів для виділення

### Опис

```methodsynopsis
public SolrQuery::getHighlightFragsize(string $field_override = ?): int
```

Повертає кількість символів фрагментів виділення. Нуль має на увазі відсутність фрагментації. Використовуйте все поле.

### Список параметрів

`field_override`

Ім'я поля

### Значення, що повертаються

Повертає ціле число у разі успішного виконання та **`null`**, якщо значення не встановлено
