---
navigation:
  - solrdocument.current.md: '« SolrDocument::current'
  - solrdocument.destruct.md: 'SolrDocument::\_\_destruct »'
  - index.md: PHP Manual
  - class.solrdocument.md: SolrDocument
title: 'SolrDocument::deleteField'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# SolrDocument::deleteField

(PECL solr >= 0.9.2)

SolrDocument::deleteField — Видаляє поле з документа

### Опис

```methodsynopsis
public SolrDocument::deleteField(string $fieldName): bool
```

Видаляє поле з документа.

### Список параметрів

`fieldName`

Назва поля

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.
