---
navigation:
  - domcharacterdata.before.md: '« DOMCharacterData::before'
  - domcharacterdata.insertdata.md: 'DOMCharacterData::insertData »'
  - index.md: PHP Manual
  - class.domcharacterdata.md: DOMCharacterData
title: 'DOMCharacterData::deleteData'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# DOMCharacterData::deleteData

(PHP 5, PHP 7, PHP 8)

DOMCharacterData::deleteData — Видалити діапазон символів із вузла

### Опис

```methodsynopsis
public DOMCharacterData::deleteData(int $offset, int $count): bool
```

Видаляє `count` символів, починаючи з позиції `offset`

### Список параметрів

`offset`

Позиція, з якої видалятимуться символи.

`count`

Кількість символів, що видаляються. Якщо `offset`и`count` у сумі виявиться більше значення довжини, буде видалено всі символи до кінця даних.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Помилки

**`DOM_INDEX_SIZE_ERR`**

Виникає, якщо `offset` менше нуля або більше кількості 16-бітних блоків у даних, або якщо `count` має від'ємне значення.

### Дивіться також

-   [DOMCharacterData::appendData()](domcharacterdata.appenddata.md) \- Додати рядок до кінця символьних даних вузла
-   [DOMCharacterData::insertData()](domcharacterdata.insertdata.md) \- Вставити рядок у вказану 16-бітну позицію
-   [DOMCharacterData::replaceData()](domcharacterdata.replacedata.md) \- Замінити підрядок у вузлі типу DOMCharacterData
-   [DOMCharacterData::substringData()](domcharacterdata.substringdata.md) \- Витягує певний діапазон даних із вузла
