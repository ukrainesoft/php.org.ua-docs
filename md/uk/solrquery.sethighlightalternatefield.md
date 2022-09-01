---
navigation:
  - solrquery.sethighlight.md: '« SolrQuery::setHighlight'
  - solrquery.sethighlightformatter.md: 'SolrQuery::setHighlightFormatter »'
  - index.md: PHP Manual
  - class.solrquery.md: SolrQuery
title: 'SolrQuery::setHighlightAlternateField'
---
# SolrQuery::setHighlightAlternateField

(PECL solr> = 0.9.2)

SolrQuery::setHighlightAlternateField — Задає поле резервного копіювання для використання

### Опис

```methodsynopsis
public SolrQuery::setHighlightAlternateField(string $field, string $field_override = ?): SolrQuery
```

Якщо фрагмент не може бути створений через відсутність відповідних виразів, можна вказати поле для використання як резервну копію або стандартне зведення.

### Список параметрів

`field`

Ім'я резервного поля

`field_override`

Ім'я поля, для якого ми перевизначаємо цей параметр.

### Значення, що повертаються

Повертає поточний об'єкт SolrQuery, якщо використовується значення, що повертається.
