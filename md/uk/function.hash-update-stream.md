---
navigation:
  - function.hash-update-file.md: « hash\_update\_file
  - function.hash-update.md: hash\_update »
  - index.md: PHP Manual
  - ref.hash.md: Функції Hash
title: hash\_update\_stream
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# hash\_update\_stream

(PHP 5 >= 5.1.2, PHP 7, PHP 8, PECL hash >= 1.1)

hash\_update\_stream — Додає дані з відкритого потоку до активного контексту хешування

### Опис

```methodsynopsis
hash_update_stream(HashContext $context, resource $stream, int $length = -1): int
```

### Список параметрів

`context`

Контекст хешування, що повертається [hash\_init()](function.hash-init.md)

`stream`

Дескриптор відкритого файлу, який повертається будь-якою функцією створення потоку.

`length`

Максимальна кількість символів для копіювання з `stream`в контекст хеширования.

### Значення, що повертаються

Фактична кількість байт, додана в контекст хешування з `stream`

### список змін

| Версия | Опис |
| --- | --- |
| 7.2.0 | Приймає [HashContext](class.hashcontext.md), а чи не ресурс. |

### Приклади

**Приклад #1 Приклад використання** hash\_update\_stream()\*\*\*\*

```php
<?php
$fp = tmpfile();
fwrite($fp, 'прыгает вокруг ленивой собаки.');

rewind($fp);

$ctx = hash_init('sha256');
hash_update($ctx, 'Наглый коричневый лисёнок ');

hash_update_stream($ctx, $fp);
echo hash_final($ctx);
?>
```

Результат виконання наведеного прикладу:

```
199f52fc9f2492c64449ed96003f135f8ea428e353e50c40b0c1a16b9c16f571
```

### Дивіться також

-   [hash\_init()](function.hash-init.md) \- Ініціалізація інкрементального контексту хешування
-   [hash\_update()](function.hash-update.md) \- Додає дані до активного контексту хешування
-   [hash\_final()](function.hash-final.md) \- Завершує інкрементальне хешування та повертає результат у вигляді хеш-коду
-   [hash()](function.hash.md) \- Генерує хеш-код (підпис повідомлення)
-   [hash\_file()](function.hash-file.md) \- Генерація хеш-значення, використовуючи вміст заданого файлу
