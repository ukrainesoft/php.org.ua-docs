Повертає кількість записів (файлів) у Phar-архіві

-   [« Phar::copy](phar.copy.md)
    
-   [Phar::createDefaultStub »](phar.createdefaultstub.md)
    
-   [PHP Manual](index.md)
    
-   [Phar](class.phar.md)
    
-   Повертає кількість записів (файлів) у Phar-архіві
    

# Phar::count

(PHP 5 >= 5.3.0, PHP 7, PHP 8, PECL phar >= 1.0.0)

Phar::count — Повертає кількість записів (файлів) у Phar-архіві

### Опис

```methodsynopsis
public Phar::count(int $mode = COUNT_NORMAL): int
```

### Список параметрів

### Значення, що повертаються

Кількість файлів, що містяться в цьому phar-архіві, або `0` (число нуль), якщо архів порожній.

### Приклади

**Приклад #1 Приклад використання **Phar::count()****

```php
<?php
// убедитесь, что архив не существует
@unlink('brandnewphar.phar');
try {
    $p = new Phar(dirname(__FILE__) . '/brandnewphar.phar', 0, 'brandnewphar.phar');
} catch (Exception $e) {
    echo 'Не удалось создать phar:', $e;
}
echo 'Новый phar содержит ' . $p->count() . " записей\n";
$p['file.txt'] = 'привет';
echo 'Новый phar содержит ' . $p->count() . " записей\n";
?>
```

Результат виконання цього прикладу:

```
Новый phar содержит 0 записей
Новый phar содержит 1 записей
```