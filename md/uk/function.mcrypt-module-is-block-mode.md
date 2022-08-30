Перевірити, чи повертає зазначений режим дані блоками чи ні

-   [« mcryptmoduleісblockalgorithm](function.mcrypt-module-is-block-algorithm.html)
    
-   [mcryptmoduleopen »](function.mcrypt-module-open.html)
    
-   [PHP Manual](index.md)
    
-   [Mcrypt](ref.mcrypt.md)
    
-   Перевірити, чи повертає зазначений режим дані блоками чи ні
    

# mcryptmoduleісblockmode

(PHP 4 >= 4.0.2, PHP 5, PHP 7 < 7.2.0, PECL mcrypt >= 1.0.0)

mcryptmoduleісblockmode — Перевірити, чи вказаний режим повертає дані блоками.

**Увага**

Ця функція оголошена *Застарілої*, починаючи з PHP 7.1.0 і була *ВИДАЛЕНО* у версії PHP 7.2.0. Використовувати цю функцію не рекомендується.

### Опис

```methodsynopsis
mcrypt_module_is_block_mode(string $mode, string $lib_dir = ?): bool
```

Функція повертає **`true`**, якщо дані повертаються блоками та \*\*`false`\*\*якщо побайтно. (тобто **`true`** для cbc та ecb, та **`false`** для cfb та потоку).

### Список параметрів

`mode`

Одна з констант **`MCRYPT_MODE_modename`**, або один з наступних рядків: "ecb", "cbc", "cfb", "ofb", "nofb" та "stream".

`lib_dir`

Опціональний параметр `lib_dir`, В якому можна вказати директорію, що містить модуль алгоритму.

### Значення, що повертаються

Функція повертає **`true`**, якщо дані повертаються блоками та **`false`** якщо побайтно. (тобто **`true`** для cbc та ecb, та **`false`** для cfb та потоку).