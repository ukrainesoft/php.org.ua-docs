---
navigation:
  - function.md5-file.md: « md5\_file
  - function.metaphone.md: metaphone »
  - index.md: PHP Manual
  - ref.strings.md: Функції для роботи з рядками
title: md5
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# md5

(PHP 4, PHP 5, PHP 7, PHP 8)

md5 - Повертає MD5-хеш рядки

**Увага**

Не рекомендується використовувати цю функцію для безпечного зберігання паролів через високу швидкість роботи цього алгоритму. Докладніше про це розказано у розділі «[Відповіді на питання, що часто ставляться з хешування паролів](faq.passwords.md#faq.passwords.fasthash)».

### Опис

```methodsynopsis
md5(string $string, bool $binary = false): string
```

Обчислює MD5-хеш рядки `string`, используя[» алгоритм MD5 RSA Data Security, Inc.](http://www.faqs.org/rfcs/rfc1321) і повертає цей хеш.

### Список параметрів

`string`

Рядок.

`binary`

Якщо необов'язковий аргумент `binary`имеет значение\*\*`true`\*\*, то повертається бінарний рядок із 16 символів.

### Значення, що повертаються

Повертає хеш у вигляді 32-символьного шістнадцяткового числа.

### Приклади

**Приклад #1 Приклад використання** md5()\*\*\*\*

```php
<?php
$str = 'яблоко';

if (md5($str) === '1afa148eb41f2e7103f21410bf48346c') {
    echo "Вам зелёное или красное яблоко?";
}
?>
```

### Дивіться також

-   [md5\_file()](function.md5-file.md) \- Повертає MD5-хеш файлу
-   [sha1\_file()](function.sha1-file.md) \- Повертає SHA1-хеш файлу
-   [crc32()](function.crc32.md) \- Обчислює поліном CRC32 для рядка
-   [sha1()](function.sha1.md) \- Повертає SHA1-хеш рядки
-   [hash()](function.hash.md) \- Генерує хеш-код (підпис повідомлення)
-   [crypt()](function.crypt.md) \- Необоротне хешування рядка
-   [password\_hash()](function.password-hash.md) \- Створює хеш пароля
