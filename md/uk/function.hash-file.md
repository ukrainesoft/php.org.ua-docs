---
navigation:
  - function.hash-equals.md: « hash\_equals
  - function.hash-final.md: hash\_final »
  - index.md: PHP Manual
  - ref.hash.md: Функції Hash
title: hash\_file
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# hash\_file

(PHP 5 >= 5.1.2, PHP 7, PHP 8, PECL hash >= 1.1)

hash\_file — Генерація хеш-значення, використовуючи вміст заданого файлу

### Опис

```methodsynopsis
hash_file(    string $algo,    string $filename,    bool $binary = false,    array $options = []): string|false
```

### Список параметрів

`algo`

Назва вибраного алгоритму хешування (наприклад, "md5", "sha256", "haval160,4" тощо). Список підтримуваних алгоритмів дивіться [hash\_algos()](function.hash-algos.md)

`filename`

Шлях або URL-адресу до файлу, який буде хешований; Підтримується інтерфейс fopen.

`binary`

Когда установлено в\*\*`true`\*\*, виводить необроблені двійкові дані При **`false`** виводить дані у шістнадцятковому кодуванні в нижньому регістрі.

`options`

Безліч опцій для різних алгоритмів хешування. В даний час у варіантах MurmurHash підтримується лише параметр "seed".

### Значення, що повертаються

Повертає рядок, що містить обчислений хеш-код у шістнадцятковому кодуванні в нижньому регістрі. Якщо `binary`задан как\*\*`true`\*\*, то повертається хеш-код у вигляді бінарних даних.

### список змін

| Версия | Опис |
| --- | --- |
| 8.1.0 | Добавлен параметр`options` |

### Приклади

**Пример #1 Использование**hash\_file()\*\*\*\*

```php
<?php
/* Создаём файл, чтобы вычислить его хеш */
file_put_contents('example.txt', 'Наглый коричневый лисёнок прыгает вокруг ленивой собаки.');

echo hash_file('sha256', 'example.txt');
?>
```

Результат виконання наведеного прикладу:

```
199f52fc9f2492c64449ed96003f135f8ea428e353e50c40b0c1a16b9c16f571
```

### Дивіться також

-   [hash()](function.hash.md) \- Генерує хеш-код (підпис повідомлення)
-   [hash\_hmac\_file()](function.hash-hmac-file.md) \- Генерація хеш-коду на основі ключа, використовуючи метод HMAC та вміст отриманого файлу
-   [hash\_update\_file()](function.hash-update-file.md) \- Додає дані з файлу до активного контексту хешування
-   [md5\_file()](function.md5-file.md) \- Повертає MD5-хеш файлу
-   [sha1\_file()](function.sha1-file.md) \- Повертає SHA1-хеш файлу
