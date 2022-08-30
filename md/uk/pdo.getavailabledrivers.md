Повертає масив доступних драйверів PDO

-   [« PDO::getAttribute](pdo.getattribute.html)
    
-   [PDO::inTransaction »](pdo.intransaction.html)
    
-   [PHP Manual](index.html)
    
-   [PDO](class.pdo.html)
    
-   Повертає масив доступних драйверів PDO
    

# PDO::getAvailableDrivers

# pdodrivers

(PHP 5> = 5.1.0, PHP 7, PHP 8, PECL pdo> = 1.0.3)

PDO::getAvailableDrivers -- pdodrivers — Повертає масив доступних драйверів PDO

### Опис

```methodsynopsis
public static PDO::getAvailableDrivers(): array
```

```methodsynopsis
pdo_drivers(): array
```

Ця функція повертає всі наявні в даний час драйвери PDO, які можна використовувати в `DSN`параметрі [PDO::construct()](pdo.construct.html)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Функція **PDO::getAvailableDrivers()** повертає масив імен PDO драйверів. Якщо немає драйверів, повертається порожній масив.

### Приклади

**Приклад #1 Приклад виконання **PDO::getAvailableDrivers()****

```php
<?php
print_r(PDO::getAvailableDrivers());
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
Array
(
    [0] => mysql
    [1] => sqlite
)
```