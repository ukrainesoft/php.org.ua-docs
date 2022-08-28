Надає значення елементу колекції

-   [« OCICollection::assign](ocicollection.assign.html)
    
-   [OCICollection::free »](ocicollection.free.html)
    
-   [PHP Manual](index.html)
    
-   [OCICollection](class.ocicollection.html)
    
-   Надає значення елементу колекції
    

# OCICollection::assignElem

(PHP 5, PHP 7, PHP 8, PECL OCI8> = 1.1.0)

OCICollection::assignElem — Надає значення елементу колекції

### Опис

```methodsynopsis
public OCICollection::assignElem(int $index, string $value): bool
```

Надає значення елементу колекції з індексом `index`

### Список параметрів

`index`

Індекс елемент. Перший індекс – нуль.

`value`

Може бути рядком чи числом.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
| 8.0.0, PECL OCI8 3.0.0 | Клас **OCI-Collection** перейменований на [OCICollection](class.ocicollection.html) відповідно до стандартів іменування PHP. |

### Дивіться також

-   [OCICollection::getElem](ocicollection.getelem.html)