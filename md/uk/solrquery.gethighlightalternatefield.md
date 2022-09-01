---
navigation:
  - solrquery.gethighlight.md: '« SolrQuery::getHighlight'
  - solrquery.gethighlightfields.md: 'SolrQuery::getHighlightFields »'
  - index.md: PHP Manual
  - class.solrquery.md: SolrQuery
title: 'SolrQuery::getHighlightAlternateField'
---
# SolrQuery::getHighlightAlternateField

(PECL solr> = 0.9.2)

SolrQuery::getHighlightAlternateField — Повертає виділене поле для використання як резервну копію або за замовчуванням

### Опис

```methodsynopsis
public SolrQuery::getHighlightAlternateField(string $field_override = ?): string
```

Повертає виділене поле для використання як резервну копію або за замовчуванням. Приймає необов'язкове перевизначення поля

### Список параметрів

`field_override`

Ім'я поля

### Значення, що повертаються

Повертає рядок у разі успішного виконання та **`null`**, якщо значення не встановлено
