---
navigation:
  - function.mcrypt-enc-get-modes-name.md: « mcryptencgetmodesname
  - function.mcrypt-enc-is-block-algorithm-mode.md: mcryptencісblockalgorithmmode »
  - index.md: PHP Manual
  - ref.mcrypt.md: Mcrypt
title: mcryptencgetsupportedkeysizes
---
# mcryptencgetsupportedkeysizes

(PHP 4 >= 4.0.2, PHP 5, PHP 7 < 7.2.0, PECL mcrypt >= 1.0.0)

mcryptencgetsupportedkeysizes — Повертає масив з допустимими розмірами ключа для алгоритму, що використовується.

**Увага**

Ця функція оголошена *Застарілої*, починаючи з PHP 7.1.0 і була *ВИДАЛЕНО* у версії PHP 7.2.0. Використовувати цю функцію не рекомендується.

### Опис

```methodsynopsis
mcrypt_enc_get_supported_key_sizes(resource $td): array
```

Повертає масив з допустимими розмірами ключа для алгоритму.

### Список параметрів

`td`

Дескриптор шифрування.

### Значення, що повертаються

Повертає масив з допустимими розмірами ключа для алгоритму. Якщо допустимі будь-які розміри від 1 до [mcryptencgetkeysize()](function.mcrypt-enc-get-key-size.md), Повертається порожній масив.

### Приклади

**Приклад #1 Приклад використання **mcryptencgetsupportedkeysizes()****

```php
<?php
    $td = mcrypt_module_open('rijndael-256', '', 'ecb', '');
    var_dump(mcrypt_enc_get_supported_key_sizes($td));
?>
```

Результат виконання цього прикладу:

```
array(3) {
  [0]=>
  int(16)
  [1]=>
  int(24)
  [2]=>
  int(32)
}
```
