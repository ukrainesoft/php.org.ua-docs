Отримує ім'я вказаного шифру

-   [« mcryptgetblocksize](function.mcrypt-get-block-size.html)
    
-   [mcryptgetвербsize »](function.mcrypt-get-iv-size.html)
    
-   [PHP Manual](index.html)
    
-   [Mcrypt](ref.mcrypt.html)
    
-   Отримує ім'я вказаного шифру
    

# mcryptgetciphername

(PHP 4, PHP 5, PHP 7 < 7.2.0, PECL mcrypt >= 1.0.0)

mcryptgetciphername — Отримує ім'я вказаного шифру

**Увага**

Ця функція оголошена *застарілої*, починаючи з PHP 7.1.0 і була *ВИДАЛЕНО* у версії PHP 7.2.0. Використовувати цю функцію не рекомендується.

### Опис

```methodsynopsis
mcrypt_get_cipher_name(int $cipher): string
```

```methodsynopsis
mcrypt_get_cipher_name(string $cipher): string
```

Функція **mcryptgetciphername()** використовується для отримання вказаного шифру.

**mcryptgetciphername()** бере номер шифру як аргумент (libmcrypt 2.2.x) або ім'я шифру (libmcrypt 2.4.x або вище) і повертає ім'я шифру або \*\*`false`\*\*якщо шифр відсутній.

### Список параметрів

`cipher`

Одна з констант **`MCRYPT_ciphername`** або назва алгоритму у вигляді рядка.

### Значення, що повертаються

Функція повертає ім'я шифру або \*\*`false`\*\*якщо такого шифру немає.

### Приклади

**Приклад #1 Приклад використання **mcryptgetciphername()****

```php
<?php
   $cipher = MCRYPT_TripleDES;

   echo mcrypt_get_cipher_name($cipher);
?>
```

Результат виконання цього прикладу:

```
3DES
```