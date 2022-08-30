Повертає список підтримуваних розмірів ключів для відкритого алгоритму

-   [« mcryptmodulegetalgokeysize](function.mcrypt-module-get-algo-key-size.html)
    
-   [mcryptmoduleісblockalgorithmmode »](function.mcrypt-module-is-block-algorithm-mode.html)
    
-   [PHP Manual](index.md)
    
-   [Mcrypt](ref.mcrypt.md)
    
-   Повертає список підтримуваних розмірів ключів для відкритого алгоритму
    

# mcryptmodulegetsupportedkeysizes

(PHP 4 >= 4.0.2, PHP 5, PHP 7 < 7.2.0, PECL mcrypt >= 1.0.0)

mcryptmodulegetsupportedkeysizes — Повертає список підтримуваних розмірів ключів для відкритого алгоритму

**Увага**

Ця функція оголошена *Застарілої*, починаючи з PHP 7.1.0 і була *ВИДАЛЕНО* у версії PHP 7.2.0. Використовувати цю функцію не рекомендується.

### Опис

```methodsynopsis
mcrypt_module_get_supported_key_sizes(string $algorithm, string $lib_dir = ?): array
```

Повертає список розмірів ключів, що підтримуються, для відкритого алгоритму. Якщо повернутий порожній масив, то підтримується будь-яка довжина ключа від 1 до значення, що повертається. [mcryptmodulegetalgokeysize()](function.mcrypt-module-get-algo-key-size.html)

### Список параметрів

`algorithm`

Використовуваний алгоритм.

`lib_dir`

Опціональний параметр `lib_dir`, В якому можна вказати директорію, що містить модуль алгоритму.

### Значення, що повертаються

Повертає список розмірів ключів, що підтримуються, для відкритого алгоритму. Якщо повернутий порожній масив, то підтримується будь-яка довжина ключа від 1 до значення, що повертається. [mcryptmodulegetalgokeysize()](function.mcrypt-module-get-algo-key-size.html)

### Дивіться також

-   [mcryptencgetsupportedkeysizes()](function.mcrypt-enc-get-supported-key-sizes.html) - Повертає масив з допустимими розмірами ключа для алгоритму