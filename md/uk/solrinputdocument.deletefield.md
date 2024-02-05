---
navigation:
  - solrinputdocument.construct.md: '« SolrInputDocument::\_\_construct'
  - solrinputdocument.destruct.md: 'SolrInputDocument::\_\_destruct »'
  - index.md: PHP Manual
  - class.solrinputdocument.md: SolrInputDocument
title: 'SolrInputDocument::deleteField'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# SolrInputDocument::deleteField

(PECL solr >= 0.9.2)

SolrInputDocument::deleteField — Видаляє поле з документа

### Опис

```methodsynopsis
public SolrInputDocument::deleteField(string $fieldName): bool
```

Видаляє поле з документа.

### Список параметрів

`fieldName`

Назва поля.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.
