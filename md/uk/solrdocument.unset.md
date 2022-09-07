---
navigation:
  - solrdocument.unserialize.md: '« SolrDocument::unserialize'
  - solrdocument.valid.md: 'SolrDocument::valid »'
  - index.md: PHP Manual
  - class.solrdocument.md: SolrDocument
title: 'SolrDocument::unset'
---
# SolrDocument::unset

(PECL solr> = 0.9.2)

SolrDocument::unset — Видалення поля з документа

### Опис

```methodsynopsis
public SolrDocument::__unset(string $fieldName): bool
```

Видаляє поле з документа, коли до поля звертаються як властивості об'єкта.

### Список параметрів

`fieldName`

Назва поля.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.
