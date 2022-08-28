Повертає максимальний розмір ключа відкритого режиму

-   [« mcrypt\_module\_get\_algo\_block\_size](function.mcrypt-module-get-algo-block-size.html)
    
-   [mcrypt\_module\_get\_supported\_key\_sizes »](function.mcrypt-module-get-supported-key-sizes.html)
    
-   [PHP Manual](index.html)
    
-   [Mcrypt](ref.mcrypt.html)
    
-   Повертає максимальний розмір ключа відкритого режиму
    

# mcryptmodulegetalgokeysize

(PHP 4 >= 4.0.2, PHP 5, PHP 7 < 7.2.0, PECL mcrypt >= 1.0.0)

mcryptmodulegetalgokeysize — Повернення максимального розміру ключа відкритого режиму

**Увага**

Ця функція оголошена *застарілої*, починаючи з PHP 7.1.0 і була *ВИДАЛЕНО* у версії PHP 7.2.0. Використовувати цю функцію не рекомендується.

### Опис

```methodsynopsis
mcrypt_module_get_algo_key_size(string $algorithm, string $lib_dir = ?): int
```

Повертає максимальний розмір ключа відкритого режиму.

### Список параметрів

`algorithm`

Ім'я алгоритму.

`lib_dir`

Опціональний параметр, у якому можна вказати директорію, що містить модуль режиму.

### Значення, що повертаються

Повертає максимальну довжину ключа у байтах для зазначеного алгоритму.