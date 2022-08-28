Вставити рядок у вказану 16-бітну позицію

-   [« DOMCharacterData::deleteData](domcharacterdata.deletedata.html)
    
-   [DOMCharacterData::replaceData »](domcharacterdata.replacedata.html)
    
-   [PHP Manual](index.html)
    
-   [DOMCharacterData](class.domcharacterdata.html)
    
-   Вставити рядок у вказану 16-бітну позицію
    

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

Функція не повертає значення після виконання.

### Помилки

**`DOM_INDEX_SIZE_ERR`**

Виникає, якщо `offset` менше нуля або більше кількості 16-бітних блоків даних.

### Дивіться також

-   [DOMCharacterData::appendData()](domcharacterdata.appenddata.html) - Додати рядок до кінця символьних даних вузла
-   [DOMCharacterData::deleteData()](domcharacterdata.deletedata.html) - Видалити діапазон символів із вузла
-   [DOMCharacterData::replaceData()](domcharacterdata.replacedata.html) - Замінити підрядок у вузлі типу DOMCharacterData
-   [DOMCharacterData::substringData()](domcharacterdata.substringdata.html) - Витягує певний діапазон даних із вузла