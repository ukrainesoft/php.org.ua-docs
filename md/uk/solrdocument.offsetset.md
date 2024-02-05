---
navigation:
  - solrdocument.offsetget.md: '« SolrDocument::offsetGet'
  - solrdocument.offsetunset.md: 'SolrDocument::offsetUnset »'
  - index.md: PHP Manual
  - class.solrdocument.md: SolrDocument
title: 'SolrDocument::offsetSet'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# SolrDocument::offsetSet

(PECL solr >= 0.9.2)

SolrDocument::offsetSet — Додає поле до документа

### Опис

```methodsynopsis
public SolrDocument::offsetSet(string $fieldName, string $fieldValue): void
```

Використовується, коли об'єкт обробляється як масив, щоб додати поле до документа.

### Список параметрів

`fieldName`

Назва поля.

`fieldValue`

Значення цього поля.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.
