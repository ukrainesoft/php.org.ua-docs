---
navigation:
  - solrquery.gethighlightformatter.md: '« SolrQuery::getHighlightFormatter'
  - solrquery.gethighlightfragsize.md: 'SolrQuery::getHighlightFragsize »'
  - index.md: PHP Manual
  - class.solrquery.md: SolrQuery
title: 'SolrQuery::getHighlightFragmenter'
---
# SolrQuery::getHighlightFragmenter

(PECL solr> = 0.9.2)

SolrQuery::getHighlightFragmenter — Повертає генератор фрагментів тексту для виділеного тексту

### Опис

```methodsynopsis
public SolrQuery::getHighlightFragmenter(string $field_override = ?): string
```

Повертає генератор фрагментів тексту виділеного тексту. Приймає необов'язкове перевизначення поля

### Список параметрів

`field_override`

Ім'я поля

### Значення, що повертаються

Повертає рядок у разі успішного виконання та **`null`**, якщо значення не встановлено
