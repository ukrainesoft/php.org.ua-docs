---
navigation:
  - solrquery.gethighlightsimplepost.md: '« SolrQuery::getHighlightSimplePost'
  - solrquery.gethighlightsnippets.md: 'SolrQuery::getHighlightSnippets »'
  - index.md: PHP Manual
  - class.solrquery.md: SolrQuery
title: 'SolrQuery::getHighlightSimplePre'
---
# SolrQuery::getHighlightSimplePre

(PECL solr> = 0.9.2)

SolrQuery::getHighlightSimplePre — Повертає текст, який з'являється перед виділеним виразом

### Опис

```methodsynopsis
public SolrQuery::getHighlightSimplePre(string $field_override = ?): string
```

Повертає текст, що з'являється перед виділеним виразом. Приймає необов'язкове перевизначення поля

### Список параметрів

`field_override`

Ім'я поля

### Значення, що повертаються

Повертає рядок у разі успішного виконання та **`null`**, якщо значення не встановлено
