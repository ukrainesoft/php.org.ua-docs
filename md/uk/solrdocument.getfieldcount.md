---
navigation:
  - solrdocument.getfield.md: '« SolrDocument::getField'
  - solrdocument.getfieldnames.md: 'SolrDocument::getFieldNames »'
  - index.md: PHP Manual
  - class.solrdocument.md: SolrDocument
title: 'SolrDocument::getFieldCount'
---
# SolrDocument::getFieldCount

(PECL solr> = 0.9.2)

SolrDocument::getFieldCount — Повертає кількість полів у цьому документі

### Опис

```methodsynopsis
public SolrDocument::getFieldCount(): int
```

Повертає кількість полів у цьому документі. Багатозначні поля враховуються лише один раз.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає ціле число у разі успішного виконання та **`false`** у разі виникнення помилки.
