---
navigation:
  - solrquery.gethighlightrequirefieldmatch.md: '« SolrQuery::getHighlightRequireFieldMatch'
  - solrquery.gethighlightsimplepre.md: 'SolrQuery::getHighlightSimplePre »'
  - index.md: PHP Manual
  - class.solrquery.md: SolrQuery
title: 'SolrQuery::getHighlightSimplePost'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# SolrQuery::getHighlightSimplePost

(PECL solr >= 0.9.2)

SolrQuery::getHighlightSimplePost — Повертає текст, який з'являється після виділеного виразу

### Опис

```methodsynopsis
public SolrQuery::getHighlightSimplePost(string $field_override = ?): string
```

Повертає текст, який з'являється після виділення. Приймає необов'язкове перевизначення поля

### Список параметрів

`field_override`

Ім'я поля

### Значення, що повертаються

Повертає рядок у разі успішного виконання та **`null`**, якщо значення не встановлено
