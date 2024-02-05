---
navigation:
  - solrdocument.unserialize.md: '« SolrDocument::unserialize'
  - solrdocument.valid.md: 'SolrDocument::valid »'
  - index.md: PHP Manual
  - class.solrdocument.md: SolrDocument
title: 'SolrDocument::\_\_unset'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# SolrDocument::\_\_unset

(PECL solr >= 0.9.2)

SolrDocument::\_\_unset — Видалення поля з документа

### Опис

```methodsynopsis
public SolrDocument::__unset(string $fieldName): bool
```

Видаляє поле з документа, коли до поля звертаються як властивості об'єкта.

### Список параметрів

`fieldName`

Назва поля.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.
