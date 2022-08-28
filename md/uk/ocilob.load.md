Повертає вміст об'єкта LOB

-   [« OCILob::import](ocilob.import.html)
    
-   [OCILob::read »](ocilob.read.html)
    
-   [PHP Manual](index.html)
    
-   [OCILob](class.ocilob.html)
    
-   Повертає вміст об'єкта LOB
    

# OCILob::load

(PHP 5, PHP 7, PHP 8, PECL OCI8> = 1.1.0)

OCILob::load — Повертає вміст об'єкта LOB

### Опис

```methodsynopsis
public OCILob::load(): string|false
```

Повертає вміст LOB. Оскільки виконання скрипта припиниться при перевищенні [memory\_limit](ini.core.html#ini.memory-limit)необхідно переконатися, що LOB не перевищує цього обмеження. Тому, в більшості випадків цей метод рекомендується замінювати на [OCILob::read](ocilob.read.html)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає вміст об'єкта або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
| 8.0.0, PECL OCI8 3.0.0 | Клас **OCI-Lob** перейменований на [OCILob](class.ocilob.html) відповідно до стандартів іменування PHP. |

### Дивіться також

-   [OCILob::read](ocilob.read.html)