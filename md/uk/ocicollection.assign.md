Надає колекції значення іншої, вже існуючої колекції

-   [« OCICollection::append](ocicollection.append.html)
    
-   [OCICollection::assignElem »](ocicollection.assignelem.html)
    
-   [PHP Manual](index.html)
    
-   [OCICollection](class.ocicollection.html)
    
-   Надає колекції значення іншої, вже існуючої колекції
    

# OCICollection::assign

(PHP 5, PHP 7, PHP 8, PECL OCI8> = 1.1.0)

OCICollection::assign — Надає колекції значення іншої, вже існуючої колекції

### Опис

```methodsynopsis
public OCICollection::assign(OCICollection $from): bool
```

Надає колекції значення іншої, раніше створеної колекції. Обидві колекції мають бути створені раніше за допомогою [oci\_new\_collection()](function.oci-new-collection.html)

### Список параметрів

`from`

Примірник OCI-Collection.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
| 8.0.0, PECL OCI8 3.0.0 | Клас **OCI-Collection** перейменований на [OCICollection](class.ocicollection.html) відповідно до стандартів іменування PHP. |

### Дивіться також

-   [OCICollection::append](ocicollection.append.html)