---
navigation:
  - solrquery.sethighlightsimplepre.md: '« SolrQuery::setHighlightSimplePre'
  - solrquery.sethighlightusephrasehighlighter.md: 'SolrQuery::setHighlightUsePhraseHighlighter »'
  - index.md: PHP Manual
  - class.solrquery.md: SolrQuery
title: 'SolrQuery::setHighlightSnippets'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# SolrQuery::setHighlightSnippets

(PECL solr >= 0.9.2)

SolrQuery::setHighlightSnippets — Встановлює максимальну кількість виділених фрагментів для створення кожного поля

### Опис

```methodsynopsis
public SolrQuery::setHighlightSnippets(int $value, string $field_override = ?): SolrQuery
```

Встановлює максимальну кількість виділених фрагментів для створення кожного поля

### Список параметрів

`value`

Максимальна кількість виділених фрагментів для створення для кожного поля

`field_override`

Ім'я поля

### Значення, що повертаються

Повертає поточний об'єкт SolrQuery, якщо використовується значення, що повертається.
