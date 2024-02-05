---
navigation:
  - domcharacterdata.after.md: '« DOMCharacterData::after'
  - domcharacterdata.before.md: 'DOMCharacterData::before »'
  - index.md: PHP Manual
  - class.domcharacterdata.md: DOMCharacterData
title: 'DOMCharacterData::appendData'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# DOMCharacterData::appendData

(PHP 5, PHP 7, PHP 8)

DOMCharacterData::appendData — Додати рядок до кінця символьних даних вузла

### Опис

```methodsynopsis
public DOMCharacterData::appendData(string $data): true
```

Добавить строку`data` в кінці символьних даних вузла.

### Список параметрів

`data`

Доданий рядок.

### Значення, що повертаються

Функція завжди повертає **`true`**

### список змін

| Версия | Опис |
| --- | --- |
| 8.3.0 | Тепер ця функція має попередній логічний (true) тип значення, що повертається. |

### Дивіться також

-   [DOMCharacterData::deleteData()](domcharacterdata.deletedata.md) \- Видалити діапазон символів із вузла
-   [DOMCharacterData::insertData()](domcharacterdata.insertdata.md) \- Вставити рядок у вказану 16-бітну позицію
-   [DOMCharacterData::replaceData()](domcharacterdata.replacedata.md) \- Замінити підрядок у вузлі типу DOMCharacterData
-   [DOMCharacterData::substringData()](domcharacterdata.substringdata.md) \- Витягує певний діапазон даних із вузла
