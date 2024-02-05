---
navigation:
  - xmlreader.isvalid.md: '« XMLReader::isValid'
  - xmlreader.movetoattribute.md: 'XMLReader::moveToAttribute »'
  - index.md: PHP Manual
  - class.xmlreader.md: XMLReader
title: 'XMLReader::lookupNamespace'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# XMLReader::lookupNamespace

(PHP 5 >= 5.1.0, PHP 7, PHP 8)

XMLReader::lookupNamespace — Знайти простір імен для префікса

### Опис

```methodsynopsis
public XMLReader::lookupNamespace(string $prefix): ?string
```

Пошук у контексті простору імен для цього префікса.

### Список параметрів

`prefix`

Рядок, що містить префікс.

### Значення, що повертаються

Значення простору імен або \*\*`null`\*\*якщо простору імен не існує.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | Функція більше не може повертати **`false`** |
