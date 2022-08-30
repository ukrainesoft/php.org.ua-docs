Витягує певний діапазон даних із вузла

-   [« DOMCharacterData::replaceData](domcharacterdata.replacedata.md)
    
-   [DOMChildNode »](class.domchildnode.md)
    
-   [PHP Manual](index.md)
    
-   [DOMCharacterData](class.domcharacterdata.md)
    
-   Витягує певний діапазон даних із вузла
    

# DOMCharacterData::substringData

(PHP 5, PHP 7, PHP 8)

DOMCharacterData::substringData — Витягує певний діапазон даних із вузла.

### Опис

```methodsynopsis
public DOMCharacterData::substringData(int $offset, int $count): string|false
```

Повертає зазначений підрядок.

### Список параметрів

`offset`

Початок позиції підрядки, що видобувається.

`count`

Кількість видобутих символів.

### Значення, що повертаються

Вказаний підрядок. Якщо `offset` і `count` у сумі перевищують довжину рядка даних вузла, будуть витягнуті всі символи остаточно рядка.

### Помилки

**`DOM_INDEX_SIZE_ERR`**

Виникає, якщо `offset` менше нуля або більше кількості 16-бітних блоків в області даних або якщо `count` має від'ємне значення.

### Дивіться також

-   [DOMCharacterData::appendData()](domcharacterdata.appenddata.md) - Додати рядок до кінця символьних даних вузла
-   [DOMCharacterData::deleteData()](domcharacterdata.deletedata.md) - Видалити діапазон символів із вузла
-   [DOMCharacterData::insertData()](domcharacterdata.insertdata.md) - Вставити рядок у вказану 16-бітну позицію
-   [DOMCharacterData::replaceData()](domcharacterdata.replacedata.md) - Замінити підрядок у вузлі типу DOMCharacterData