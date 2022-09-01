---
navigation:
  - solrdocument.unserialize.html: '« SolrDocument::unserialize'
  - solrdocument.valid.html: 'SolrDocument::valid »'
  - index.html: PHP Manual
  - class.solrdocument.html: SolrDocument
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
