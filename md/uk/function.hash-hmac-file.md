---
navigation:
  - function.hash-hmac-algos.md: « hash\_hmac\_algos
  - function.hash-hmac.md: hash\_hmac »
  - index.md: PHP Manual
  - ref.hash.md: Функції Hash
title: hash\_hmac\_file
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# hash\_hmac\_file

(PHP 5 >= 5.1.2, PHP 7, PHP 8, PECL hash >= 1.1)

hash\_hmac\_file — Генерація хеш-коду на основі ключа, використовуючи метод HMAC та вміст отриманого файлу

### Опис

```methodsynopsis
hash_hmac_file(    string $algo,    string $filename,    string $key,    bool $binary = false): string|false
```

### Список параметрів

`algo`

Ім'я вибраного алгоритму хешування (наприклад, "md5", "sha256", "haval160,4" тощо) Дивіться [hash\_hmac\_algos()](function.hash-hmac-algos.md) для отримання списку алгоритмів, що підтримуються.

`filename`

URL розташування файлу для хешування; Підтримуються обробники Fopen.

`key`

Загальний секретний ключ, який використовується для генерації HMAC хеш-коду.

`binary`

Когда установлено в\*\*`true`\*\*, виводить необроблені двійкові дані При **`false`** виводить дані у шістнадцятковому кодуванні в нижньому регістрі.

### Значення, що повертаються

Повертає рядок, що містить обчислений хеш-код у шістнадцятковому кодуванні в нижньому регістрі. Якщо `binary`задан как\*\*`true`\*\*, то повертається хеш-код у вигляді бінарних даних. Повертає **`false`**, якщо файл `filename`недоступен для чтения.

### Помилки

Викидає виняток [ValueError](class.valueerror.md), якщо параметр `algo` невідомий чи не є криптографічною хеш-функцією.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | Тепер викидає виняток [ValueError](class.valueerror.md), якщо алгоритм `algo` невідомий чи не є криптографічною хеш-функцією; раніше натомість поверталося значення **`false`** |
| 7.2.0 | Заборонено використання некриптографічних хеш-функцій (adler32, crc32, crc32b, fnv132, fnv1a32, fnv164, fnv1a64, joaat). |

### Приклади

**Приклад #1 Приклад використання** hash\_hmac\_file()\*\*\*\*

```php
<?php
/* Создаём файл, чтобы вычислить его хеш */
file_put_contents('example.txt', 'Наглый коричневый лисёнок прыгает вокруг ленивой собаки.');

echo hash_hmac_file('sha256', 'example.txt', 'secret');
?>
```

Результат виконання наведеного прикладу:

```
bc83c8fabc807cabbbb087bf90c760888349b223b5ba0a35251f7b37b05bf9c9
```

### Дивіться також

-   [hash\_hmac\_algos()](function.hash-hmac-algos.md) \- Повертає список зареєстрованих алгоритмів хешування, які застосовуються для hash\_hmac
-   [hash\_hmac()](function.hash-hmac.md) \- Генерація хеш-коду на основі ключа, використовуючи метод HMAC
-   [hash\_file()](function.hash-file.md) \- Генерація хеш-значення, використовуючи вміст заданого файлу
