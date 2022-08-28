Перемістити позицію курсору на наступний атрибут

-   [« XMLReader::moveToFirstAttribute](xmlreader.movetofirstattribute.html)
    
-   [XMLReader::next »](xmlreader.next.html)
    
-   [PHP Manual](index.html)
    
-   [XMLReader](class.xmlreader.html)
    
-   Перемістити позицію курсору на наступний атрибут
    

# XMLReader::moveToNextAttribute

(PHP 5> = 5.1.0, PHP 7, PHP 8)

XMLReader::moveToNextAttribute — Перемістити позицію курсору на наступний атрибут

### Опис

```methodsynopsis
public XMLReader::moveToNextAttribute(): bool
```

Переміщує курсор до наступного атрибута, якщо курсор спозиційований на атрибуті або переміщує позицію на перший атрибут, якщо спозиціоновано на елементі.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [XMLReader::moveToElement()](xmlreader.movetoelement.html) - Позиціонувати курсор на батьківському елементі поточного атрибуту
-   [XMLReader::moveToAttribute()](xmlreader.movetoattribute.html) - Перемістити курсор до атрибуту із заданим ім'ям
-   [XMLReader::moveToAttributeNo()](xmlreader.movetoattributeno.html) - Перемістити курсор на атрибут за індексом
-   [XMLReader::moveToAttributeNs()](xmlreader.movetoattributens.html) - Перемістити курсор до іменованого атрибуту
-   [XMLReader::moveToFirstAttribute()](xmlreader.movetofirstattribute.html) - Перемістити позицію курсору на перший атрибут