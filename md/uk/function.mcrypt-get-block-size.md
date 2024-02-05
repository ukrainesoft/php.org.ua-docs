---
navigation:
  - function.mcrypt-generic.md: « mcrypt\_generic
  - function.mcrypt-get-cipher-name.md: mcrypt\_get\_cipher\_name »
  - index.md: PHP Manual
  - ref.mcrypt.md: Mcrypt
title: mcrypt\_get\_block\_size
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# mcrypt\_get\_block\_size

(PHP 4, PHP 5, PHP 7 < 7.2.0, PECL mcrypt >= 1.0.0)

mcrypt\_get\_block\_size — Повертає розмір блоку для зазначеного шифру

**Увага**

Ця функція оголошена *застарілої* починаючи з PHP 7.1.0 і була *ВИДАЛЕНО* у версії PHP 7.2.0. Використовувати цю функцію не рекомендується.

### Опис

```methodsynopsis
mcrypt_get_block_size(int $cipher): int|false
```

```methodsynopsis
mcrypt_get_block_size(string $cipher, string $mode): int|false
```

Перший зразок зібраний з бібліотекою libmcrypt 2.2.x, а другий з libmcrypt 2.4.x або 2.5.x.

**mcrypt\_get\_block\_size()** використовується для отримання розміру блоку вказаного `cipher` (У комбінації з режимом шифрування).

Правильніше використовувати [mcrypt\_enc\_get\_block\_size()](function.mcrypt-enc-get-block-size.md), яка використовує ресурс, що повертається [mcrypt\_module\_open()](function.mcrypt-module-open.md)

### Список параметрів

`cipher`

Одна из констант\*\*`MCRYPT_ciphername`\*\*или название алгоритма в виде строки.

`mode`

Одна из констант\*\*`MCRYPT_MODE_modename`\*\*, або один з наступних рядків: "ecb", "cbc", "cfb", "ofb", "nofb" та "stream".

### Значення, що повертаються

Повертає розмір блоку алгоритму в байтах або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Пример #1 Пример использования**mcrypt\_get\_block\_size()\*\*\*\*

Цей приклад демонструє використання функції, зібраної з libmcrypt 2.4.x і 2.5.x.

```php
<?php

echo mcrypt_get_block_size('tripledes', 'ecb'); // 8

?>
```

### Дивіться також

-   [mcrypt\_get\_key\_size()](function.mcrypt-get-key-size.md) \- Отримати розмір ключа заданого шифру
-   [mcrypt\_enc\_get\_block\_size()](function.mcrypt-enc-get-block-size.md) \- Повертає розмір блоку алгоритму
-   [mcrypt\_encrypt()](function.mcrypt-encrypt.md) \- Шифрує текст із заданими параметрами
