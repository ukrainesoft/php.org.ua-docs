---
navigation:
  - domcharacterdata.deletedata.md: '« DOMCharacterData::deleteData'
  - domcharacterdata.remove.md: 'DOMCharacterData::remove »'
  - index.md: PHP Manual
  - class.domcharacterdata.md: DOMCharacterData
title: 'DOMCharacterData::insertData'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# DOMCharacterData::insertData

(PHP 5, PHP 7, PHP 8)

DOMCharacterData::insertData — Вставити рядок у вказану 16-бітну позицію

### Опис

```methodsynopsis
public DOMCharacterData::insertData(int $offset, string $data): bool
```

Вставляє рядок `data` у позицію `offset`

### Список параметрів

`offset`

Позиція символу, з якого буде вставлено рядок.

`data`

Рядок, що вставляється.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Помилки

**`DOM_INDEX_SIZE_ERR`**

Виникає, якщо `offset` менше нуля або більше кількості 16-бітних блоків даних.

### Дивіться також

-   [DOMCharacterData::appendData()](domcharacterdata.appenddata.md) \- Додати рядок до кінця символьних даних вузла
-   [DOMCharacterData::deleteData()](domcharacterdata.deletedata.md) \- Видалити діапазон символів із вузла
-   [DOMCharacterData::replaceData()](domcharacterdata.replacedata.md) \- Замінити підрядок у вузлі типу DOMCharacterData
-   [DOMCharacterData::substringData()](domcharacterdata.substringdata.md) \- Витягує певний діапазон даних із вузла
