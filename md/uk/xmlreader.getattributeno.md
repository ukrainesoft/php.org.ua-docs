Отримати значення атрибута за індексом

-   [« XMLReader::getAttribute](xmlreader.getattribute.html)
    
-   [XMLReader::getAttributeNs »](xmlreader.getattributens.html)
    
-   [PHP Manual](index.html)
    
-   [XMLReader](class.xmlreader.html)
    
-   Отримати значення атрибута за індексом
    

# XMLReader::getAttributeNo

(PHP 5> = 5.1.0, PHP 7, PHP 8)

XMLReader::getAttributeNo — Отримати значення атрибута за індексом

### Опис

```methodsynopsis
public XMLReader::getAttributeNo(int $index): ?string
```

Повертає значення атрибута на основі позиції або порожній рядок, якщо атрибут не існує або не розташований на вузлі елемента.

### Список параметрів

`index`

Позиція атрибуту.

### Значення, що повертаються

Значення атрибуту або або **`null`**, якщо атрибут із заданим параметром `index` не існує чи ні позиції елемента.

### Дивіться також

-   [XMLReader::getAttribute()](xmlreader.getattribute.html) - Отримати значення атрибута з певним ім'ям
-   [XMLReader::getAttributeNs()](xmlreader.getattributens.html) - Отримати значення атрибуту по localname та URI