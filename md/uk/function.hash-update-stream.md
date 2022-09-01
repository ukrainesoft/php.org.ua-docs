---
navigation:
  - function.hash-update-file.html: « hashupdatefile
  - function.hash-update.html: hashupdate »
  - index.md: PHP Manual
  - ref.hash.md: Функции Hash
title: hashupdatestream
---
# hashupdatestream

(PHP 5> = 5.1.2, PHP 7, PHP 8, PECL hash> = 1.1)

hashupdatestream — Додає дані з відкритого потоку до активного контексту хешування

### Опис

```methodsynopsis
hash_update_stream(HashContext $context, resource $stream, int $length = -1): int
```

### Список параметрів

`context`

Контекст хешування, що повертається [hashinit()](function.hash-init.md)

`stream`

Дескриптор відкритого файлу, який повертається будь-якою функцією створення потоку.

`length`

Максимальна кількість символів для копіювання з `stream` у контекст хешування.

### Значення, що повертаються

Фактична кількість байт, додана в контекст хешування з `stream`

### список змін

| Версия | Описание |
| --- | --- |
|  | Приймає [HashContext](class.hashcontext.md), а чи не ресурс. |

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

-   [hashinit()](function.hash-init.md) - Ініціалізація інкрементального контексту хешування
-   [hashupdate()](function.hash-update.md) - Додає дані до активного контексту хешування
-   [hashfinal()](function.hash-final.md) - Завершує інкрементальне хешування та повертає результат у вигляді хеш-коду
-   [hash()](function.hash.md) - Генерує хеш-код (підпис повідомлення)
-   [hashfile()](function.hash-file.md) - Генерація хеш-значення, використовуючи вміст заданого файлу
