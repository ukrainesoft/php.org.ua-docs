Перемістити курсор до іменованого атрибуту

-   [« XMLReader::moveToAttributeNo](xmlreader.movetoattributeno.html)
    
-   [XMLReader::moveToElement »](xmlreader.movetoelement.html)
    
-   [PHP Manual](index.html)
    
-   [XMLReader](class.xmlreader.html)
    
-   Перемістити курсор до іменованого атрибуту
    

# XMLReader::moveToAttributeNs

(PHP 5> = 5.1.0, PHP 7, PHP 8)

XMLReader::moveToAttributeNs — Перемістити курсор до іменованого атрибуту

### Опис

```methodsynopsis
public XMLReader::moveToAttributeNs(string $name, string $namespace): bool
```

Позиціонує курсор на іменованому атрибуті у вказаному просторі імен.

### Список параметрів

`name`

Місцеве ім'я.

`namespace`

URI простір імен.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [XMLReader::moveToElement()](xmlreader.movetoelement.html) - Позиціонувати курсор на батьківському елементі поточного атрибуту
-   [XMLReader::moveToAttribute()](xmlreader.movetoattribute.html) - Перемістити курсор до атрибуту із заданим ім'ям
-   [XMLReader::moveToAttributeNo()](xmlreader.movetoattributeno.html) - Перемістити курсор на атрибут за індексом
-   [XMLReader::moveToFirstAttribute()](xmlreader.movetofirstattribute.html) - Перемістити позицію курсору на перший атрибут