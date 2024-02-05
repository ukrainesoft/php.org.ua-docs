---
navigation:
  - function.mcrypt-enc-get-modes-name.md: « mcrypt\_enc\_get\_modes\_name
  - function.mcrypt-enc-is-block-algorithm-mode.md: mcrypt\_enc\_is\_block\_algorithm\_mode »
  - index.md: PHP Manual
  - ref.mcrypt.md: Mcrypt
title: mcrypt\_enc\_get\_supported\_key\_sizes
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# mcrypt\_enc\_get\_supported\_key\_sizes

(PHP 4 >= 4.0.2, PHP 5, PHP 7 < 7.2.0, PECL mcrypt >= 1.0.0)

mcrypt\_enc\_get\_supported\_key\_sizes — Повертає масив з допустимими розмірами ключа для алгоритму, що використовується.

**Увага**

Ця функція оголошена *застарілої* починаючи з PHP 7.1.0 і була *ВИДАЛЕНО* у версії PHP 7.2.0. Використовувати цю функцію не рекомендується.

### Опис

```methodsynopsis
mcrypt_enc_get_supported_key_sizes(resource $td): array
```

Повертає масив з допустимими розмірами ключа для алгоритму.

### Список параметрів

`td`

Дескриптор шифрування.

### Значення, що повертаються

Повертає масив з допустимими розмірами ключа для алгоритму. Якщо допустимі будь-які розміри від 1 до [mcrypt\_enc\_get\_key\_size()](function.mcrypt-enc-get-key-size.md), Повертається порожній масив.

### Приклади

**Пример #1 Пример использования**mcrypt\_enc\_get\_supported\_key\_sizes()\*\*\*\*

```php
<?php
    $td = mcrypt_module_open('rijndael-256', '', 'ecb', '');
    var_dump(mcrypt_enc_get_supported_key_sizes($td));
?>
```

Результат виконання наведеного прикладу:

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
