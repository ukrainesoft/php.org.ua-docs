Повертає розмір блоку для зазначеного шифру

-   [« mcryptgeneric](function.mcrypt-generic.html)
    
-   [mcryptgetciphername »](function.mcrypt-get-cipher-name.html)
    
-   [PHP Manual](index.html)
    
-   [Mcrypt](ref.mcrypt.html)
    
-   Повертає розмір блоку для зазначеного шифру
    

# mcryptgetblocksize

(PHP 4, PHP 5, PHP 7 < 7.2.0, PECL mcrypt >= 1.0.0)

mcryptgetblocksize — Повертає розмір блоку для зазначеного шифру

**Увага**

Ця функція оголошена *Застарілої*, починаючи з PHP 7.1.0 і була *ВИДАЛЕНО* у версії PHP 7.2.0. Використовувати цю функцію не рекомендується.

### Опис

```methodsynopsis
mcrypt_get_block_size(int $cipher): int|false
```

```methodsynopsis
mcrypt_get_block_size(string $cipher, string $mode): int|false
```

Перший зразок зібраний з бібліотекою libmcrypt 2.2.x, а другий з libmcrypt 2.4.x або 2.5.x.

**mcryptgetblocksize()** використовується для отримання розміру блоку вказаного `cipher` (У комбінації з режимом шифрування).

Правильніше використовувати [mcryptencgetblocksize()](function.mcrypt-enc-get-block-size.html), яка використовує ресурс, що повертається [mcryptmoduleopen()](function.mcrypt-module-open.html)

### Список параметрів

`cipher`

Одна з констант **`MCRYPT_ciphername`** або назва алгоритму у вигляді рядка.

`mode`

Одна з констант **`MCRYPT_MODE_modename`**, або один з наступних рядків: "ecb", "cbc", "cfb", "ofb", "nofb" та "stream".

### Значення, що повертаються

Повертає розмір блоку алгоритму в байтах або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **mcryptgetblocksize()****

Цей приклад демонструє використання функції зібраної з libmcrypt 2.4.x та 2.5.x.

```php
<?php

echo mcrypt_get_block_size('tripledes', 'ecb'); // 8

?>
```

### Дивіться також

-   [mcryptgetkeysize()](function.mcrypt-get-key-size.html) - Отримати розмір ключа заданого шифру
-   [mcryptencgetblocksize()](function.mcrypt-enc-get-block-size.html) - Повертає розмір блоку алгоритму
-   [mcryptencrypt()](function.mcrypt-encrypt.html) - Шифрує текст із заданими параметрами