---
navigation:
  - function.sha1-file.html: « sha1file
  - function.similar-text.html: similartext »
  - index.md: PHP Manual
  - ref.strings.md: Функції для роботи з рядками
title: sha1
---
# sha1

(PHP 4> = 4.3.0, PHP 5, PHP 7, PHP 8)

sha1 - Повертає SHA1-хеш рядки

**Увага**

Не рекомендується використовувати цю функцію для забезпечення безпеки зберігання паролів через високу швидкість роботи даного алгоритму. Докладніше читайте у розділі [Відповіді на найчастіші запитання щодо шифрування паролів](faq.passwords.html#faq.passwords.fasthash)

### Опис

```methodsynopsis
sha1(string $string, bool $binary = false): string
```

Повертає SHA1-хеш рядки `string`, обчислений за алгоритмом [» US Secure Hash Algorithm 1](http://www.faqs.org/rfcs/rfc3174)

### Список параметрів

`string`

Вхідний рядок.

`binary`

Якщо необов'язковий аргумент `binary` має значення **`true`**, хеш повертається у вигляді бінарного рядка з 20 символів, інакше його буде повернено у вигляді 40-символьного шістнадцяткового числа.

### Значення, що повертаються

Повертає SHA1-хеш у вигляді рядка.

### Приклади

**Приклад #1 Приклад використання **sha1()****

```php
<?php
$str = 'яблоко';

if (sha1($str) === '88b184adea10bf987b15257a5d6c5cb94eba69d3') {
    echo "Желаете зелёное или красное яблоко?";
}
?>
```

### Дивіться також

-   [sha1file()](function.sha1-file.html) - Повертає SHA1-хеш файлу
-   [crc32()](function.crc32.md) - Обчислює поліном CRC32 для рядка
-   [md5()](function.md5.md) - Повертає MD5-хеш рядки
-   [hash()](function.hash.md) - Генерує хеш-код (підпис повідомлення)
-   [crypt()](function.crypt.md) - Необоротне хешування рядка
-   [passwordhash()](function.password-hash.html) - Створює хеш пароля
