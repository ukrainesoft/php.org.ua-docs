---
navigation:
  - function.sha1-file.md: « sha1\_file
  - function.similar-text.md: similar\_text »
  - index.md: PHP Manual
  - ref.strings.md: Функції для роботи з рядками
title: sha1
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# sha1

(PHP 4 >= 4.3.0, PHP 5, PHP 7, PHP 8)

sha1 - Повертає SHA1-хеш рядки

**Увага**

Не рекомендується використовувати цю функцію для безпечного зберігання паролів через високу швидкість роботи цього алгоритму. Докладніше про це розказано у розділі «[Відповіді на питання, що часто ставляться з хешування паролів](faq.passwords.md#faq.passwords.fasthash)».

### Опис

```methodsynopsis
sha1(string $string, bool $binary = false): string
```

Повертає SHA1-хеш рядки `string`, обчислений за алгоритмом [» US Secure Hash Algorithm 1](http://www.faqs.org/rfcs/rfc3174)

### Список параметрів

`string`

Вхідний рядок.

`binary`

Якщо необов'язковий аргумент `binary`имеет значение\*\*`true`\*\*, хеш повертається у вигляді бінарного рядка з 20 символів, інакше його буде повернено у вигляді 40-символьного шістнадцяткового числа.

### Значення, що повертаються

Повертає SHA1-хеш у вигляді рядка.

### Приклади

**Приклад #1 Приклад використання** sha1()\*\*\*\*

```php
<?php
$str = 'яблоко';

if (sha1($str) === '88b184adea10bf987b15257a5d6c5cb94eba69d3') {
    echo "Желаете зелёное или красное яблоко?";
}
?>
```

### Дивіться також

-   [sha1\_file()](function.sha1-file.md) \- Повертає SHA1-хеш файлу
-   [crc32()](function.crc32.md) \- Обчислює поліном CRC32 для рядка
-   [md5()](function.md5.md) \- Повертає MD5-хеш рядки
-   [hash()](function.hash.md) \- Генерує хеш-код (підпис повідомлення)
-   [crypt()](function.crypt.md) \- Необоротне хешування рядка
-   [password\_hash()](function.password-hash.md) \- Створює хеш пароля
