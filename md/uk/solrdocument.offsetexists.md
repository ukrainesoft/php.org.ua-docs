---
navigation:
  - solrdocument.next.md: '« SolrDocument::next'
  - solrdocument.offsetget.md: 'SolrDocument::offsetGet »'
  - index.md: PHP Manual
  - class.solrdocument.md: SolrDocument
title: 'SolrDocument::offsetExists'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# SolrDocument::offsetExists

(PECL solr >= 0.9.2)

SolrDocument::offsetExists — Перевіряє, чи існує конкретне поле

### Опис

```methodsynopsis
public SolrDocument::offsetExists(string $fieldName): bool
```

Перевіряє, чи існує певне поле. Використовується, коли об'єкт обробляється масивом.

### Список параметрів

`fieldName`

Назва поля.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.
