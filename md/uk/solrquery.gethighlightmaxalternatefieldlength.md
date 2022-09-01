---
navigation:
  - solrquery.gethighlighthighlightmultiterm.md: '« SolrQuery::getHighlightHighlightMultiTerm'
  - solrquery.gethighlightmaxanalyzedchars.md: 'SolrQuery::getHighlightMaxAnalyzedChars »'
  - index.md: PHP Manual
  - class.solrquery.md: SolrQuery
title: 'SolrQuery::getHighlightMaxAlternateFieldLength'
---
# SolrQuery::getHighlightMaxAlternateFieldLength

(PECL solr> = 0.9.2)

SolrQuery::getHighlightMaxAlternateFieldLength — Повертає максимальну кількість символів поля для повернення

### Опис

```methodsynopsis
public SolrQuery::getHighlightMaxAlternateFieldLength(string $field_override = ?): int
```

Повертає максимальну кількість символів поля для повернення

### Список параметрів

`field_override`

Ім'я поля

### Значення, що повертаються

Повертає ціле число у разі успішного виконання та **`null`**, якщо значення не встановлено
