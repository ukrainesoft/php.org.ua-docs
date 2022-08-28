Встановіть іменовану точку збереження транзакції

-   [« mysqli::rollback](mysqli.rollback.html)
    
-   [mysqli::select\_db »](mysqli.select-db.html)
    
-   [PHP Manual](index.html)
    
-   [mysqli](class.mysqli.html)
    
-   Встановіть іменовану точку збереження транзакції
    

# mysqli::savepoint

# mysqlisavepoint

(PHP 5> = 5.5.0, PHP 7, PHP 8)

mysqli::savepoint -- mysqlisavepoint — Встановіть іменовану точку збереження транзакції.

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public mysqli::savepoint(string $name): bool
```

Процедурний стиль:

```methodsynopsis
mysqli_savepoint(mysqli $mysql, string $name): bool
```

Функція ідентична до виконання запиту ``$mysqli->query("SAVEPOINT `$name`");``

### Список параметрів

`mysql`

Тільки для процедурного стилю: об'єкт [mysqli](class.mysqli.html), отриманий за допомогою [mysqli\_connect()](function.mysqli-connect.html) або [mysqli\_init()](mysqli.init.html)

`name`

Ідентифікатор точки збереження.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [mysqli\_release\_savepoint()](mysqli.release-savepoint.html) - Видаляє іменовану точку збереження зі списку точок збереження поточної транзакції