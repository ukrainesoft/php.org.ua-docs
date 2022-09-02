---
navigation:
  - solrdocument.getchilddocumentscount.md: '« SolrDocument::getChildDocumentsCount'
  - solrdocument.getfieldcount.md: 'SolrDocument::getFieldCount »'
  - index.md: PHP Manual
  - class.solrdocument.md: SolrDocument
title: 'SolrDocument::getField'
---
# SolrDocument::getField

(PECL solr> = 0.9.2)

SolrDocument::getField — Отримує поле на ім'я

### Опис

```methodsynopsis
public SolrDocument::getField(string $fieldName): SolrDocumentField
```

Отримує поле на ім'я.

### Список параметрів

`fieldName`

Назва поля.

### Значення, що повертаються

Повертає SolrDocumentField у разі успішного виконання та **`false`** у разі виникнення помилки.
