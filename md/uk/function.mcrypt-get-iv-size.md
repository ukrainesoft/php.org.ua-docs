---
navigation:
  - function.mcrypt-get-cipher-name.md: « mcrypt\_get\_cipher\_name
  - function.mcrypt-get-key-size.md: mcrypt\_get\_key\_size »
  - index.md: PHP Manual
  - ref.mcrypt.md: Mcrypt
title: mcrypt\_get\_iv\_size
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# mcrypt\_get\_iv\_size

(PHP 4 >= 4.0.2, PHP 5, PHP 7 < 7.2.0, PECL mcrypt >= 1.0.0)

mcrypt\_get\_iv\_size — Повертає розмір вектора, що ініціалізує, для відповідної комбінації шифру та режиму

**Увага**

Ця функція оголошена *застарілої* починаючи з PHP 7.1.0 і була *ВИДАЛЕНО* у версії PHP 7.2.0. Використовувати цю функцію не рекомендується.

### Опис

```methodsynopsis
mcrypt_get_iv_size(string $cipher, string $mode): int
```

Повертає розмір вектора, що ініціалізує, для відповідної заданої комбінації шифру. `cipher`и режима`mode`

Правильніше використовуватиме [mcrypt\_enc\_get\_iv\_size()](function.mcrypt-enc-get-iv-size.md), тому що вона повертає результат по існуючому дескриптору шифрування, отриманого за допомогою [mcrypt\_module\_open()](function.mcrypt-module-open.md)

### Список параметрів

`cipher`

Одна из констант\*\*`MCRYPT_ciphername`\*\*или название алгоритма в виде строки.

`mode`

Одна из констант\*\*`MCRYPT_MODE_modename`\*\*, або один з наступних рядків: "ecb", "cbc", "cfb", "ofb", "nofb" та "stream".

Ініціативний вектор ігнорується в режимі ECB, оскільки він там не потрібен. Вам знадобиться той самий ініціалізуючий вектор як для шифрування, так і для дешифрування, інакше все ваше шифрування перетвориться на гарбуз.

### Значення, що повертаються

Повертає розмір вектора, що ініціалізує, в байтах. У разі виникнення помилки буде повернено **`false`**. Якщо при заданій комбінації шифру та режиму ініціалізуючий вектор не потрібен, буде повернено нуль.

### Приклади

**Приклад #1 Приклад використання** mcrypt\_get\_iv\_size()\*\*\*\*

```php
<?php
    echo mcrypt_get_iv_size(MCRYPT_CAST_256, MCRYPT_MODE_CFB) . "\n";

    echo mcrypt_get_iv_size('des', 'ecb') . "\n";
?>
```

### Дивіться також

-   [mcrypt\_get\_block\_size()](function.mcrypt-get-block-size.md) \- Повертає розмір блоку для зазначеного шифру
-   [mcrypt\_enc\_get\_iv\_size()](function.mcrypt-enc-get-iv-size.md) \- Повертає розмір вектора, що ініціалізує, для алгоритму
-   [mcrypt\_create\_iv()](function.mcrypt-create-iv.md) \- Створити ініціалізуючий вектор (Initialization Vector або IV) із випадкового джерела
