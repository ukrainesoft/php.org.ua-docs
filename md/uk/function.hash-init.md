---
navigation:
  - function.hash-hmac.md: « hash\_hmac
  - function.hash-pbkdf2.md: hash\_pbkdf2 »
  - index.md: PHP Manual
  - ref.hash.md: Функції Hash
title: hash\_init
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# hash\_init

(PHP 5 >= 5.1.2, PHP 7, PHP 8, PECL hash >= 1.1)

hash\_init - Ініціалізація інкрементального контексту хешування

### Опис

```methodsynopsis
hash_init(    string $algo,    int $flags = 0,    string $key = "",    array $options = []): HashContext
```

### Список параметрів

`algo`

Ім'я обраного алгоритму хешування (наприклад, "md5", "sha256", "haval160,4" тощо). Увесь список підтримуваних алгоритмів можна переглянути в описі функції [hash\_algos()](function.hash-algos.md)

`flags`

Необов'язкові налаштування для генерації хешу, в даний час підтримується лише один варіант: **`HASH_HMAC`**. При цьому параметр `key` *повинен* бути вказано.

`key`

Якщо \*\*`HASH_HMAC`\*\*указан в параметре`flags`, то в цьому параметрі потрібно надати загальний секретний ключ, який використовуватиметься з методом хешування HMAC.

`options`

Безліч опцій для різних алгоритмів хешування. В даний час у варіантах MurmurHash підтримується лише параметр "seed".

### Значення, що повертаються

Повертає контекст хешування для використання у функціях [hash\_update()](function.hash-update.md) [hash\_update\_stream()](function.hash-update-stream.md) [hash\_update\_file()](function.hash-update-file.md) і [hash\_final()](function.hash-final.md)

### Помилки

Викидає виняток [ValueError](class.valueerror.md), якщо параметр `algo` невідомий або не є криптографічною хеш-функцією або якщо параметр `key`не задан.

### список змін

| Версия | Опис |
| --- | --- |
| 8.1.0 | Добавлен параметр`options` |
| 8.0.0 | Тепер викидає виняток [ValueError](class.valueerror.md), якщо параметр `algo` невідомий або не є криптографічною хеш-функцією або якщо параметр `key` не заданий; раніше поверталося значення **`false`** і видавалася помилка рівня **`E_WARNING`**. emitted. |
| 7.2.0 | Заборонено використання некриптографічних хеш-функцій (adler32, crc32, crc32b, fnv132, fnv1a32, fnv164, fnv1a64, joaat) з константою **`HASH_HMAC`** |
| 7.2.0 | Повертає [HashContext](class.hashcontext.md), а чи не ресурс. |

### Приклади

**Приклад #1 Приклад інкрементального хешування**

```php
<?php
$hash = hash('sha256', 'Наглый коричневый лисёнок прыгает вокруг ленивой собаки.');

$ctx = hash_init('sha256');

hash_update($ctx, 'Наглый коричневый лисёнок ');
hash_update($ctx, 'прыгает вокруг ленивой собаки.');

$incremental_hash = hash_final($ctx);

echo $incremental_hash, PHP_EOL;
var_dump($hash === $incremental_hash);
?>
```

Результат виконання наведеного прикладу:

```
199f52fc9f2492c64449ed96003f135f8ea428e353e50c40b0c1a16b9c16f571
bool(true)
```

### Дивіться також

-   [hash()](function.hash.md) \- Генерує хеш-код (підпис повідомлення)
-   [hash\_algos()](function.hash-algos.md) \- Повертає список зареєстрованих алгоритмів хешування
-   [hash\_file()](function.hash-file.md) \- Генерація хеш-значення, використовуючи вміст заданого файлу
-   [hash\_hmac()](function.hash-hmac.md) \- Генерація хеш-коду на основі ключа, використовуючи метод HMAC
-   [hash\_hmac\_file()](function.hash-hmac-file.md) \- Генерація хеш-коду на основі ключа, використовуючи метод HMAC та вміст отриманого файлу
