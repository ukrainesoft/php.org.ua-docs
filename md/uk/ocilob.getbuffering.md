Повертає стан буферизації великого об'єкта (LOB)

-   [« OCILob::free](ocilob.free.html)
    
-   [OCILob::import »](ocilob.import.html)
    
-   [PHP Manual](index.html)
    
-   [OCILob](class.ocilob.html)
    
-   Повертає стан буферизації великого об'єкта (LOB)
    

# OCILob::getBuffering

(PHP 5, PHP 7, PHP 8, PECL OCI8> = 1.1.0)

OCILob::getBuffering — Повертає поточний стан буферизації великого об'єкта (LOB)

### Опис

```methodsynopsis
public OCILob::getBuffering(): bool
```

Повідомляє, чи увімкнена буферизація для великого об'єкта (LOB).

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає **`false`**, якщо буферизація вимкнена, та **`true`**, якщо увімкнено.

### список змін

| Версия | Описание |
| --- | --- |
| 8.0.0, PECL OCI8 3.0.0 | Клас **OCI-Lob** перейменований на [OCILob](class.ocilob.html) відповідно до стандартів іменування PHP. |

### Дивіться також

-   [OCILob::setBuffering](ocilob.setbuffering.html)