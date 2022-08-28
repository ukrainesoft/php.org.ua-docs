Видаляє файл усередині phar-архіву

-   [« Phar::delMetadata](phar.delmetadata.html)
    
-   [Phar::\_\_destruct »](phar.destruct.html)
    
-   [PHP Manual](index.html)
    
-   [Phar](class.phar.html)
    
-   Видаляє файл усередині phar-архіву
    

# Phar::delete

(PHP 5 >= 5.3.0, PHP 7, PHP 8, PECL phar >= 2.0.0)

Phar::delete — Видалення файлу всередині phar-архіву

### Опис

```methodsynopsis
public Phar::delete(string $localName): bool
```

> **Зауваження**
> 
> Для коректної роботи з об'єктами [Phar](class.phar.html) цьому методу необхідне встановлення значення php.ini `phar.readonly` в `0`. В іншому випадку, буде викинуто виняток [PharException](class.pharexception.html)

Видаляє файл із архіву. Ця функція аналогічна виклику [unlink()](function.unlink.html) для обгортки потоку, як показано в прикладі нижче.

### Список параметрів

`localName`

Шлях всередині архіву для видалення файлу.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання, але краще перевірити, чи було викинуто виняток, і вважати успішним виклик, у результаті якого викинуто виняток.

### Помилки

Викидає виняток [PharException](class.pharexception.html), якщо виникли помилки під час запису змін на диск.

### Приклади

**Приклад #1 Приклад використання **Phar::delete()****

```php
<?php
try {
    $phar = new Phar('myphar.phar');
    $phar->delete('удали/меня.php');
    // это эквивалентно следующему:
    unlink('phar://myphar.phar/удали/меня.php');
} catch (Exception $e) {
    // обработка ошибок
}
?>
```

### Дивіться також

-   [PharData::delete()](phardata.delete.html) - Видалити файл із tar/zip-архіву
-   [Phar::unlinkArchive()](phar.unlinkarchive.html) - Повністю видалити архів з пам'яті та з диска