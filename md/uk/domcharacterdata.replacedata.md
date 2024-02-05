---
navigation:
  - domcharacterdata.remove.md: '« DOMCharacterData::remove'
  - domcharacterdata.replacewith.md: 'DOMCharacterData::replaceWith »'
  - index.md: PHP Manual
  - class.domcharacterdata.md: DOMCharacterData
title: 'DOMCharacterData::replaceData'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# DOMCharacterData::replaceData

(PHP 5, PHP 7, PHP 8)

DOMCharacterData::replaceData — Замінити підрядок у вузлі типу DOMCharacterData

### Опис

```methodsynopsis
public DOMCharacterData::replaceData(int $offset, int $count, string $data): bool
```

Замінює `count` символів, починаючи з позиції `offset`, на строку`data`

### Список параметрів

`offset`

Позиція, з якої розпочинається заміна.

`count`

Кількість символів для заміни. Якщо `offset`и`count` у сумі перевищують довжину рядка даних, замінять всі символи до кінця даних.

`data`

Рядок, на який буде проводитись заміна.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Помилки

**`DOM_INDEX_SIZE_ERR`**

Виникає, якщо `offset` менше нуля або більше кількості 16-бітних блоків в області даних, або якщо `count` має від'ємне значення.

### Дивіться також

-   [DOMCharacterData::appendData()](domcharacterdata.appenddata.md) \- Додати рядок до кінця символьних даних вузла
-   [DOMCharacterData::deleteData()](domcharacterdata.deletedata.md) \- Видалити діапазон символів із вузла
-   [DOMCharacterData::insertData()](domcharacterdata.insertdata.md) \- Вставити рядок у вказану 16-бітну позицію
-   [DOMCharacterData::substringData()](domcharacterdata.substringdata.md) \- Витягує певний діапазон даних із вузла
