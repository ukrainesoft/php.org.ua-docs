---
navigation:
  - solrquery.gethighlightsimplepre.md: '« SolrQuery::getHighlightSimplePre'
  - solrquery.gethighlightusephrasehighlighter.md: 'SolrQuery::getHighlightUsePhraseHighlighter »'
  - index.md: PHP Manual
  - class.solrquery.md: SolrQuery
title: 'SolrQuery::getHighlightSnippets'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# SolrQuery::getHighlightSnippets

(PECL solr >= 0.9.2)

SolrQuery::getHighlightSnippets — Повертає максимальну кількість виділених фрагментів для створення кожного поля

### Опис

```methodsynopsis
public SolrQuery::getHighlightSnippets(string $field_override = ?): int
```

Повертає максимальну кількість виділених фрагментів для створення кожного поля. Приймає необов'язкове перевизначення поля

### Список параметрів

`field_override`

Ім'я поля

### Значення, що повертаються

Повертає ціле число у разі успішного виконання та **`null`**, якщо значення не встановлено.
