Повертає ім'я алгоритму

-   [« mcrypt\_decrypt](function.mcrypt-decrypt.html)
    
-   [mcrypt\_enc\_get\_block\_size »](function.mcrypt-enc-get-block-size.html)
    
-   [PHP Manual](index.html)
    
-   [Mcrypt](ref.mcrypt.html)
    
-   Повертає ім'я алгоритму
    

# mcryptencgetalgorithmsname

(PHP 4 >= 4.0.2, PHP 5, PHP 7 < 7.2.0, PECL mcrypt >= 1.0.0)

mcryptencgetalgorithmsname — Повертає ім'я алгоритму

**Увага**

Ця функція оголошена *застарілої*, починаючи з PHP 7.1.0 і була *ВИДАЛЕНО* у версії PHP 7.2.0. Використовувати цю функцію не рекомендується.

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

**Приклад #1 Приклад використання **mcryptencgetalgorithmsname()****

```php
<?php
$td = mcrypt_module_open(MCRYPT_CAST_256, '', MCRYPT_MODE_CFB, '');
echo mcrypt_enc_get_algorithms_name($td). "\n";

$td = mcrypt_module_open('cast-256', '', MCRYPT_MODE_CFB, '');
echo mcrypt_enc_get_algorithms_name($td). "\n";
?>
```

Результат виконання цього прикладу:

```
CAST-256
CAST-256
```