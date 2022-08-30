Функція запускає самоперевірку вказаного модуля

-   [« mcryptmoduleopen](function.mcrypt-module-open.html)
    
-   [mdecryptgeneric »](function.mdecrypt-generic.html)
    
-   [PHP Manual](index.html)
    
-   [Mcrypt](ref.mcrypt.html)
    
-   Функція запускає самоперевірку вказаного модуля
    

# mcryptmoduleselftest

(PHP 4 >= 4.0.2, PHP 5, PHP 7 < 7.2.0, PECL mcrypt >= 1.0.0)

mcryptmoduleselftest — Функція запускає самоперевірку вказаного модуля

**Увага**

Ця функція оголошена *Застарілої*, починаючи з PHP 7.1.0 і була *ВИДАЛЕНО* у версії PHP 7.2.0. Використовувати цю функцію не рекомендується.

### Опис

```methodsynopsis
mcrypt_module_self_test(string $algorithm, string $lib_dir = ?): bool
```

Ця функція запускає самоперевірку вказаного алгоритму.

### Список параметрів

`algorithm`

Одна з констант **`MCRYPT_ciphername`** або назва алгоритму у вигляді рядка.

`lib_dir`

Опціональний параметр `lib_dir`, В якому можна вказати директорію, що містить модуль алгоритму.

### Значення, що повертаються

Ця функція повертає **`true`** якщо самоперевірка завершилася успішно та **`false`**, якщо ні.

### Приклади

**Приклад #1 Приклад використання **mcryptmoduleselftest()****

```php
<?php
var_dump(mcrypt_module_self_test(MCRYPT_RIJNDAEL_128)) . "\n";
var_dump(mcrypt_module_self_test(MCRYPT_BOGUS_CYPHER));
?>
```

Результат виконання цього прикладу:

```
bool(true)
bool(false)
```