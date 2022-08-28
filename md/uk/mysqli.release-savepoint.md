Видаляє іменовану точку збереження зі списку точок збереження поточної транзакції

-   [« mysqli::refresh](mysqli.refresh.html)
    
-   [mysqli::rollback »](mysqli.rollback.html)
    
-   [PHP Manual](index.html)
    
-   [mysqli](class.mysqli.html)
    
-   Видаляє іменовану точку збереження зі списку точок збереження поточної транзакції
    

# mysqli::releasesavepoint

# mysqlireleasesavepoint

(PHP 5> = 5.5.0, PHP 7, PHP 8)

mysqli::releasesavepoint - mysqlireleasesavepoint — Видалити іменовану точку збереження зі списку точок збереження поточної транзакції.

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public mysqli::release_savepoint(string $name): bool
```

Процедурний стиль:

```methodsynopsis
mysqli_release_savepoint(mysqli $mysql, string $name): bool
```

Функція ідентична до виконання запиту ``$mysqli->query("RELEASE SAVEPOINT `$name`");``. Вона не запускає фіксацію чи відкат.

### Список параметрів

`mysql`

Тільки для процедурного стилю: об'єкт [mysqli](class.mysqli.html), отриманий за допомогою [mysqli\_connect()](function.mysqli-connect.html) або [mysqli\_init()](mysqli.init.html)

`name`

Ідентифікатор точки збереження.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [mysqli\_savepoint()](mysqli.savepoint.html) - Встановіть іменовану точку збереження транзакції