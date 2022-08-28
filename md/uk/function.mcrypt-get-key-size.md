Отримати розмір ключа заданого шифру

-   [« mcrypt\_get\_iv\_size](function.mcrypt-get-iv-size.html)
    
-   [mcrypt\_list\_algorithms »](function.mcrypt-list-algorithms.html)
    
-   [PHP Manual](index.html)
    
-   [Mcrypt](ref.mcrypt.html)
    
-   Отримати розмір ключа заданого шифру
    

# mcryptgetkeysize

(PHP 4, PHP 5, PHP 7 < 7.2.0, PECL mcrypt >= 1.0.0)

mcryptgetkeysize — Отримати розмір ключа заданого шифру

**Увага**

Ця функція оголошена *застарілої*, починаючи з PHP 7.1.0 і була *ВИДАЛЕНО* у версії PHP 7.2.0. Використовувати цю функцію не рекомендується.

### Опис

```methodsynopsis
mcrypt_get_key_size(int $cipher): int|false
```

```methodsynopsis
mcrypt_get_key_size(string $cipher, string $mode): int|false
```

Перший зразок зібраний з бібліотекою libmcrypt 2.2.x, а другий з libmcrypt 2.4.x або 2.5.x.

**mcryptgetkeysize()** використовується для отримання розміру ключа для зазначеного шифру `cipher` (У комбінації з режимом шифрування).

Правильніше використовуватиме [mcrypt\_enc\_get\_key\_size()](function.mcrypt-enc-get-key-size.html), тому що вона повертає результат по існуючому дескриптору шифрування, отриманого за допомогою [mcrypt\_module\_open()](function.mcrypt-module-open.html)

### Список параметрів

`cipher`

Одна з констант **`MCRYPT_ciphername`** або назва алгоритму у вигляді рядка.

`mode`

Одна з констант **`MCRYPT_MODE_modename`**, або один з наступних рядків: "ecb", "cbc", "cfb", "ofb", "nofb" та "stream".

### Значення, що повертаються

Повертає максимально допустиму довжину ключа в байтах або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **mcryptgetkeysize()****

```php
<?php
    echo mcrypt_get_key_size('tripledes', 'ecb');
?>
```

Цей приклад демонструє використання функції зібраної з libmcrypt 2.4.x та 2.5.x.

Результат виконання цього прикладу:

```
24
```

### Дивіться також

-   [mcrypt\_get\_block\_size()](function.mcrypt-get-block-size.html) - Повертає розмір блоку для зазначеного шифру
-   [mcrypt\_enc\_get\_key\_size()](function.mcrypt-enc-get-key-size.html) - Повертає максимальну допустиму довжину ключа алгоритму
-   [mcrypt\_encrypt()](function.mcrypt-encrypt.html) - Шифрує текст із заданими параметрами