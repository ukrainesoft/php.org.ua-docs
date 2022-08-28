Додає дані з відкритого потоку до активного контексту хешування

-   [« hash\_update\_file](function.hash-update-file.html)
    
-   [hash\_update »](function.hash-update.html)
    
-   [PHP Manual](index.html)
    
-   [Функции Hash](ref.hash.html)
    
-   Додає дані з відкритого потоку до активного контексту хешування
    

# hashupdatestream

(PHP 5> = 5.1.2, PHP 7, PHP 8, PECL hash> = 1.1)

hashupdatestream — Додає дані з відкритого потоку до активного контексту хешування

### Опис

```methodsynopsis
hash_update_stream(HashContext $context, resource $stream, int $length = -1): int
```

### Список параметрів

`context`

Контекст хешування, що повертається [hash\_init()](function.hash-init.html)

`stream`

Дескриптор відкритого файлу, який повертається будь-якою функцією створення потоку.

`length`

Максимальна кількість символів для копіювання з `stream` у контекст хешування.

### Значення, що повертаються

Фактична кількість байт, додана в контекст хешування з `stream`

### список змін

| Версия | Описание |
| --- | --- |
|  | Приймає [HashContext](class.hashcontext.html), а чи не ресурс. |

### Приклади

**Приклад #1 Приклад використання **hashupdatestream()****

```php
<?php
$fp = tmpfile();
fwrite($fp, 'Наглый коричневый лисёнок прыгает вокруг ленивой собаки.');
rewind($fp);

$ctx = hash_init('md5');
hash_update_stream($ctx, $fp);
echo hash_final($ctx);
?>
```

Результат виконання цього прикладу:

```
bff8b4bc8b5c1c1d5b3211dfb21d1e76
```

### Дивіться також

-   [hash\_init()](function.hash-init.html) - Ініціалізація інкрементального контексту хешування
-   [hash\_update()](function.hash-update.html) - Додає дані до активного контексту хешування
-   [hash\_final()](function.hash-final.html) - Завершує інкрементальне хешування та повертає результат у вигляді хеш-коду
-   [hash()](function.hash.html) - Генерує хеш-код (підпис повідомлення)
-   [hash\_file()](function.hash-file.html) - Генерація хеш-значення, використовуючи вміст заданого файлу