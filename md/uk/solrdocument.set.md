---
navigation:
  - solrdocument.serialize.md: '« SolrDocument::serialize'
  - solrdocument.sort.md: 'SolrDocument::sort »'
  - index.md: PHP Manual
  - class.solrdocument.md: SolrDocument
title: 'SolrDocument::\_\_set'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# SolrDocument::\_\_set

(PECL solr >= 0.9.2)

SolrDocument::\_\_set — Додає ще одне поле до документа

### Опис

```methodsynopsis
public SolrDocument::__set(string $fieldName, string $fieldValue): bool
```

Додає ще одне поле до документа. Використовується для встановлення полів як нові властивості.

### Список параметрів

`fieldName`

Назва поля.

`fieldValue`

Значення поля.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.
