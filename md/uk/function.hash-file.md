---
navigation:
  - function.hash-equals.md: « hashequals
  - function.hash-final.md: hashfinal »
  - index.md: PHP Manual
  - ref.hash.md: Функции Hash
title: hashfile
---
# hashfile

(PHP 5> = 5.1.2, PHP 7, PHP 8, PECL hash> = 1.1)

hashfile — Генерація хеш-значення, використовуючи вміст заданого файлу

### Опис

```methodsynopsis
hash_file(    string $algo,    string $filename,    bool $binary = false,    array $options = []): string|false
```

### Список параметрів

`algo`

Назва вибраного алгоритму хешування (наприклад, "md5", "sha256", "haval160,4" тощо). Список підтримуваних алгоритмів дивіться [hashalgos()](function.hash-algos.md)

`filename`

Шлях або URL-адресу до файлу, який буде хешований; Підтримується інтерфейс fopen.

`binary`

Коли встановлено в **`true`**, виводить необроблені двійкові дані При **`false`** виводить дані у шістнадцятковому кодуванні в нижньому регістрі.

`options`

Безліч опцій для різних алгоритмів хешування. В даний час у варіантах MurmurHash підтримується лише параметр "seed".

### Значення, що повертаються

Повертає рядок, що містить обчислений хеш-код у шістнадцятковому кодуванні в нижньому регістрі. Якщо `binary` заданий як **`true`**, то повертається хеш-код у вигляді бінарних даних.

### список змін

| Версия | Описание |
| --- | --- |
|  | Доданий параметр `options` |

### Приклади

**Приклад #1 Використання **hashfile()****

```php
<?php
/* Создаём файл, чтобы вычислить его хеш */
file_put_contents('example.txt', 'Наглый коричневый лисёнок прыгает вокруг ленивой собаки.');

echo hash_file('md5', 'example.txt');
?>
```

Результат виконання цього прикладу:

```
bff8b4bc8b5c1c1d5b3211dfb21d1e76
```

### Дивіться також

-   [hash()](function.hash.md) - Генерує хеш-код (підпис повідомлення)
-   [hashhmacfile()](function.hash-hmac-file.md) - Генерація хеш-коду на основі ключа, використовуючи метод HMAC та вміст отриманого файлу
-   [hashupdatefile()](function.hash-update-file.md) - Додає дані з файлу до активного контексту хешування
-   [md5file()](function.md5-file.md) - Повертає MD5-хеш файлу
-   [sha1file()](function.sha1-file.md) - Повертає SHA1-хеш файлу
