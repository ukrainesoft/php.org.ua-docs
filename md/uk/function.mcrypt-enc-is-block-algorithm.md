Перевіряє, чи використовує алгоритм блокові режими

-   [« mcryptencісblockalgorithmmode](function.mcrypt-enc-is-block-algorithm-mode.html)
    
-   [mcryptencісblockmode »](function.mcrypt-enc-is-block-mode.html)
    
-   [PHP Manual](index.html)
    
-   [Mcrypt](ref.mcrypt.html)
    
-   Перевіряє, чи використовує алгоритм блокові режими
    

# mcryptencісblockalgorithm

(PHP 4 >= 4.0.2, PHP 5, PHP 7 < 7.2.0, PECL mcrypt >= 1.0.0)

mcryptencісblockalgorithm - Перевіряє, чи використовує алгоритм блокові режими

**Увага**

Ця функція оголошена *Застарілої*, починаючи з PHP 7.1.0 і була *ВИДАЛЕНО* у версії PHP 7.2.0. Використовувати цю функцію не рекомендується.

### Опис

```methodsynopsis
mcrypt_enc_is_block_algorithm(resource $td): bool
```

Перевіряє, чи використовує алгоритм блокові режими.

### Список параметрів

`td`

Дескриптор шифрування.

### Значення, що повертаються

Повертає \*\*`true`\*\*якщо алгоритм є блоковим або \*\*`false`\*\*якщо потоковий.