---
navigation:
  - class.solrdocument.md: « SolrDocument
  - solrdocument.clear.md: 'SolrDocument::clear »'
  - index.md: PHP Manual
  - class.solrdocument.md: SolrDocument
title: 'SolrDocument::addField'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# SolrDocument::addField

(PECL solr >= 0.9.2)

SolrDocument::addField — Додає поле до документа

### Опис

```methodsynopsis
public SolrDocument::addField(string $fieldName, string $fieldValue): bool
```

Метод додає поле до екземпляра SolrDocument.

### Список параметрів

`fieldName`

Назва поля

`fieldValue`

Значення поля.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.
