---
navigation:
  - function.mcrypt-decrypt.md: « mcrypt\_decrypt
  - function.mcrypt-enc-get-block-size.md: mcrypt\_enc\_get\_block\_size »
  - index.md: PHP Manual
  - ref.mcrypt.md: Mcrypt
title: mcrypt\_enc\_get\_algorithms\_name
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# mcrypt\_enc\_get\_algorithms\_name

(PHP 4 >= 4.0.2, PHP 5, PHP 7 < 7.2.0, PECL mcrypt >= 1.0.0)

mcrypt\_enc\_get\_algorithms\_name — Повертає ім'я алгоритму

**Увага**

Ця функція оголошена *застарілої* починаючи з PHP 7.1.0 і була *ВИДАЛЕНО* у версії PHP 7.2.0. Використовувати цю функцію не рекомендується.

### Опис

```methodsynopsis
mcrypt_enc_get_algorithms_name(resource $td): string
```

Ця функція повертає назву алгоритму.

### Список параметрів

`td`

Дескриптор шифрування.

### Значення, що повертаються

Повертає ім'я відкритого алгоритму у вигляді рядка.

### Приклади

**Приклад #1 Приклад використання** mcrypt\_enc\_get\_algorithms\_name()\*\*\*\*

```php
<?php
$td = mcrypt_module_open(MCRYPT_CAST_256, '', MCRYPT_MODE_CFB, '');
echo mcrypt_enc_get_algorithms_name($td). "\n";

$td = mcrypt_module_open('cast-256', '', MCRYPT_MODE_CFB, '');
echo mcrypt_enc_get_algorithms_name($td). "\n";
?>
```

Результат виконання наведеного прикладу:

```
CAST-256
CAST-256
```
