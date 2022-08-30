Отримати значення атрибута з певним ім'ям

-   [« XMLReader::expand](xmlreader.expand.md)
    
-   [XMLReader::getAttributeNo »](xmlreader.getattributeno.md)
    
-   [PHP Manual](index.md)
    
-   [XMLReader](class.xmlreader.md)
    
-   Отримати значення атрибута з певним ім'ям
    

# XMLReader::getAttribute

(PHP 5> = 5.1.0, PHP 7, PHP 8)

XMLReader::getAttribute — Отримати значення атрибуту з певним ім'ям

### Опис

```methodsynopsis
public XMLReader::getAttribute(string $name): ?string
```

Повертає значення іменованого атрибуту або \*\*`null`\*\*якщо атрибут не існує або не знаходиться у вузлі елемента.

### Список параметрів

`name`

Ім'я атрибуту.

### Значення, що повертаються

Значення атрибуту або **`null`**, якщо атрибут із заданим параметром `name` не знайдено чи немає позиції елемента.

### список змін

| Версия | Описание |
| --- | --- |
|  | Функція більше не може повертати **`false`** |

### Дивіться також

-   [XMLReader::getAttributeNo()](xmlreader.getattributeno.md) - Отримати значення атрибуту за індексом
-   [XMLReader::getAttributeNs()](xmlreader.getattributens.md) - Отримати значення атрибуту по localname та URI