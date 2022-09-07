---
navigation:
  - solrinputdocument.addchilddocuments.md: '« SolrInputDocument::addChildDocuments'
  - solrinputdocument.clear.md: 'SolrInputDocument::clear »'
  - index.md: PHP Manual
  - class.solrinputdocument.md: SolrInputDocument
title: 'SolrInputDocument::addField'
---
# SolrInputDocument::addField

(PECL solr> = 0.9.2)

SolrInputDocument::addField — Додає поле до документа

### Опис

```methodsynopsis
public SolrInputDocument::addField(string $fieldName, string $fieldValue, float $fieldBoostValue = 0.0): bool
```

Для багатозначних полів, якщо вказано допустиме значення підвищення, вказане значення буде помножено на поточне значення підвищення поля.

### Список параметрів

`fieldName`

Назва поля

`fieldValue`

Значення поля.

`fieldBoostValue`

Індекс збільшення часу поля. Хоча він не може бути негативним, ви все одно можете передавати значення менше 1.0, але вони повинні бути більшими за нуль.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.
