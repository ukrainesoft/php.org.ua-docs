---
navigation:
  - function.mcrypt-enc-get-key-size.md: « mcryptencgetkeysize
  - function.mcrypt-enc-get-supported-key-sizes.md: mcryptencgetsupportedkeysizes »
  - index.md: PHP Manual
  - ref.mcrypt.md: Mcrypt
title: mcryptencgetmodesname
---
# mcryptencgetmodesname

(PHP 4 >= 4.0.2, PHP 5, PHP 7 < 7.2.0, PECL mcrypt >= 1.0.0)

mcryptencgetmodesname — Повертає ім'я режиму, що використовується.

**Увага**

Ця функція оголошена *Застарілої*, починаючи з PHP 7.1.0 і була *ВИДАЛЕНО* у версії PHP 7.2.0. Використовувати цю функцію не рекомендується.

### Опис

```methodsynopsis
mcrypt_enc_get_modes_name(resource $td): string
```

Повертає ім'я режиму.

### Список параметрів

`td`

Дескриптор шифрування.

### Значення, що повертаються

Повертає ім'я режиму у вигляді рядка.

### Приклади

**Приклад #1 Приклад використання **mcryptencgetmodesname()****

```php
<?php
$td = mcrypt_module_open (MCRYPT_CAST_256, '', MCRYPT_MODE_CFB, '');
echo mcrypt_enc_get_modes_name($td). "\n";

$td = mcrypt_module_open ('cast-256', '', 'ecb', '');
echo mcrypt_enc_get_modes_name($td). "\n";
?>
```

Результат виконання цього прикладу:

```
CFB
ECB
```
