Перевіряє, чи заданий алгоритм є блоковим чи ні

-   [« mcryptmoduleісblockalgorithmmode](function.mcrypt-module-is-block-algorithm-mode.html)
    
-   [mcryptmoduleісblockmode »](function.mcrypt-module-is-block-mode.html)
    
-   [PHP Manual](index.md)
    
-   [Mcrypt](ref.mcrypt.md)
    
-   Перевіряє, чи заданий алгоритм є блоковим чи ні
    

# mcryptmoduleісblockalgorithm

(PHP 4 >= 4.0.2, PHP 5, PHP 7 < 7.2.0, PECL mcrypt >= 1.0.0)

mcryptmoduleісblockalgorithm — Перевіряє, чи заданий алгоритм є блоковим чи ні.

**Увага**

Ця функція оголошена *застарілої*, починаючи з PHP 7.1.0 і була *ВИДАЛЕНО* у версії PHP 7.2.0. Використовувати цю функцію не рекомендується.

### Опис

```methodsynopsis
mcrypt_module_is_block_algorithm(string $algorithm, string $lib_dir = ?): bool
```

Функція повертає \*\*`true`\*\*якщо алгоритм блоковий, інакше повертає **`false`** (Потоковий).

### Список параметрів

`algorithm`

Алгоритм для перевірки

`lib_dir`

Опціональний параметр `lib_dir`, В якому можна вказати директорію, що містить модуль алгоритму.

### Значення, що повертаються

Функція повертає \*\*`true`\*\*якщо алгоритм блоковий, інакше повертає **`false`** (Потоковий).