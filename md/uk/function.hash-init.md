---
navigation:
  - function.hash-hmac.md: « hashhmac
  - function.hash-pbkdf2.md: hashpbkdf2 »
  - index.md: PHP Manual
  - ref.hash.md: Функции Hash
title: hashinit
---
# hashinit

(PHP 5> = 5.1.2, PHP 7, PHP 8, PECL hash> = 1.1)

hashinit - Ініціалізація інкрементального контексту хешування

### Опис

```methodsynopsis
hash_init(    string $algo,    int $flags = 0,    string $key = "",    array $options = []): HashContext
```

### Список параметрів

`algo`

Ім'я обраного алгоритму хешування (наприклад, "md5", "sha256", "haval160,4" тощо). Увесь список підтримуваних алгоритмів можна переглянути в описі функції [hashalgos()](function.hash-algos.md)

`flags`

Необов'язкові налаштування для генерації хешу, в даний час підтримується лише один варіант: **`HASH_HMAC`**. При цьому параметр `key` *повинен* бути вказано.

`key`

Якщо **`HASH_HMAC`** вказано у параметрі `flags`, то в цьому параметрі потрібно надати загальний секретний ключ, який використовуватиметься з методом хешування HMAC.

`options`

Безліч опцій для різних алгоритмів хешування. В даний час у варіантах MurmurHash підтримується лише параметр "seed".

### Значення, що повертаються

Повертає контекст хешування для використання у функціях [hashupdate()](function.hash-update.md) [hashupdatestream()](function.hash-update-stream.md) [hashupdatefile()](function.hash-update-file.md) і [hashfinal()](function.hash-final.md)

### список змін

| Версия | Описание |
| --- | --- |
|  | Доданий параметр `options` |
|  | Заборонено використання некриптографічних хеш-функцій (adler32, crc32, crc32b, fnv132, fnv1a32, fnv164, fnv1a64, joaat) з константою **`HASH_HMAC`** |
|  | Повертає [HashContext](class.hashcontext.md), а чи не ресурс. |

### Приклади

**Приклад #1 Приклад інкрементального хешування**

```php
<?php
$ctx = hash_init('md5');
hash_update($ctx, 'Наглый коричневый лисёнок ');
hash_update($ctx, 'прыгает вокруг ленивой собаки.');
echo hash_final($ctx);
?>
```

Результат виконання цього прикладу:

```
bff8b4bc8b5c1c1d5b3211dfb21d1e76
```

### Дивіться також

-   [hash()](function.hash.md) - Генерує хеш-код (підпис повідомлення)
-   [hashalgos()](function.hash-algos.md) - Повертає список зареєстрованих алгоритмів хешування
-   [hashfile()](function.hash-file.md) - Генерація хеш-значення, використовуючи вміст заданого файлу
-   [hashhmac()](function.hash-hmac.md) - Генерація хеш-коду на основі ключа, використовуючи метод HMAC
-   [hashhmacfile()](function.hash-hmac-file.md) - Генерація хеш-коду на основі ключа, використовуючи метод HMAC та вміст отриманого файлу
