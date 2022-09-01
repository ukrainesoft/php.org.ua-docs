---
navigation:
  - domcharacterdata.appenddata.html: '« DOMCharacterData::appendData'
  - domcharacterdata.insertdata.html: 'DOMCharacterData::insertData »'
  - index.html: PHP Manual
  - class.domcharacterdata.html: DOMCharacterData
title: 'DOMCharacterData::deleteData'
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

Кількість символів, що видаляються. Якщо `offset` і `count` у сумі виявиться більше значення довжини, буде видалено всі символи до кінця даних.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Помилки

**`DOM_INDEX_SIZE_ERR`**

Виникає, якщо `offset` менше нуля або більше кількості 16-бітних блоків у даних, або якщо `count` має від'ємне значення.

### Дивіться також

-   [DOMCharacterData::appendData()](domcharacterdata.appenddata.html) - Додати рядок до кінця символьних даних вузла
-   [DOMCharacterData::insertData()](domcharacterdata.insertdata.html) - Вставити рядок у вказану 16-бітну позицію
-   [DOMCharacterData::replaceData()](domcharacterdata.replacedata.html) - Замінити підрядок у вузлі типу DOMCharacterData
-   [DOMCharacterData::substringData()](domcharacterdata.substringdata.html) - Витягує певний діапазон даних із вузла
