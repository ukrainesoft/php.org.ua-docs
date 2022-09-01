---
navigation:
  - solrinputdocument.construct.md: '« SolrInputDocument::construct'
  - solrinputdocument.destruct.md: 'SolrInputDocument::destruct »'
  - index.md: PHP Manual
  - class.solrinputdocument.md: SolrInputDocument
title: 'SolrInputDocument::deleteField'
---
# SolrInputDocument::deleteField

(PECL solr> = 0.9.2)

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

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.
