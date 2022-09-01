---
navigation:
  - function.mcrypt-get-cipher-name.html: « mcryptgetciphername
  - function.mcrypt-get-key-size.html: mcryptgetkeysize »
  - index.html: PHP Manual
  - ref.mcrypt.html: Mcrypt
title: mcryptgetвербsize
---
# mcryptgetвербsize

(PHP 4 >= 4.0.2, PHP 5, PHP 7 < 7.2.0, PECL mcrypt >= 1.0.0)

mcryptgetвербsize — Повертає розмір вектора, що ініціалізує, для відповідної комбінації шифру та режиму

**Увага**

Ця функція оголошена *застарілої*, починаючи з PHP 7.1.0 і була *ВИДАЛЕНО* у версії PHP 7.2.0. Використовувати цю функцію не рекомендується.

### Опис

```methodsynopsis
mcrypt_get_iv_size(string $cipher, string $mode): int
```

Повертає розмір вектора, що ініціалізує, для відповідної заданої комбінації шифру. `cipher` та режиму `mode`

Правильніше використовуватиме [mcryptencgetвербsize()](function.mcrypt-enc-get-iv-size.html), тому що вона повертає результат по існуючому дескриптору шифрування, отриманого за допомогою [mcryptmoduleopen()](function.mcrypt-module-open.html)

### Список параметрів

`cipher`

Одна з констант **`MCRYPT_ciphername`** або назва алгоритму у вигляді рядка.

`mode`

Одна з констант **`MCRYPT_MODE_modename`**, або один з наступних рядків: "ecb", "cbc", "cfb", "ofb", "nofb" та "stream".

Ініціативний вектор ігнорується в режимі ECB, оскільки він там не потрібен. Вам знадобиться той самий ініціалізуючий вектор як для шифрування, так і для дешифрування, інакше все ваше шифрування перетвориться на гарбуз.

### Значення, що повертаються

Повертає розмір вектора, що ініціалізує, в байтах. У разі виникнення помилки буде повернено **`false`**. Якщо при заданій комбінації шифру та режиму ініціалізуючий вектор не потрібен, буде повернено нуль.

### Приклади

**Приклад #1 Приклад використання **mcryptgetвербsize()****

```php
<?php
    echo mcrypt_get_iv_size(MCRYPT_CAST_256, MCRYPT_MODE_CFB) . "\n";

    echo mcrypt_get_iv_size('des', 'ecb') . "\n";
?>
```

### Дивіться також

-   [mcryptgetblocksize()](function.mcrypt-get-block-size.html) - Повертає розмір блоку для зазначеного шифру
-   [mcryptencgetвербsize()](function.mcrypt-enc-get-iv-size.html) - Повертає розмір вектора, що ініціалізує, для алгоритму
-   [mcryptcreateiv()](function.mcrypt-create-iv.html) - Створити ініціалізуючий вектор (Initialization Vector або IV) із випадкового джерела
