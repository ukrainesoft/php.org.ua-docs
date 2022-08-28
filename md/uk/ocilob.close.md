Закриває дескриптор об'єкта LOB

-   [« OCILob::append](ocilob.append.html)
    
-   [OCILob::eof »](ocilob.eof.html)
    
-   [PHP Manual](index.html)
    
-   [OCILob](class.ocilob.html)
    
-   Закриває дескриптор об'єкта LOB
    

# OCILob::close

(PHP 5, PHP 7, PHP 8, PECL OCI8> = 1.1.0)

OCILob::close — Закриває дескриптор об'єкта LOB

### Опис

```methodsynopsis
public OCILob::close(): bool
```

Закриває дескриптор об'єкта LOB чи FILE. Функцію слід використовувати лише разом із [OCILob::writeTemporary](ocilob.writetemporary.html)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия                 | Описание                                                                                                |
|------------------------|---------------------------------------------------------------------------------------------------------|
| 8.0.0, PECL OCI8 3.0.0 | Клас **OCI-Lob** перейменований на [OCILob](class.ocilob.html) відповідно до стандартів іменування PHP. |

### Дивіться також

-   [OCILob::writeTemporary](ocilob.writetemporary.html)