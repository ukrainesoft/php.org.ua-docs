Отримати список усіх підтримуваних алгоритмів шифрування

-   [« mcrypt\_get\_key\_size](function.mcrypt-get-key-size.html)
    
-   [mcrypt\_list\_modes »](function.mcrypt-list-modes.html)
    
-   [PHP Manual](index.html)
    
-   [Mcrypt](ref.mcrypt.html)
    
-   Отримати список усіх підтримуваних алгоритмів шифрування
    

# mcryptlistalgorithms

(PHP 4 >= 4.0.2, PHP 5, PHP 7 < 7.2.0, PECL mcrypt >= 1.0.0)

mcryptlistalgorithms — Отримати список усіх підтримуваних алгоритмів шифрування

**Увага**

Ця функція оголошена *Застарілої*, починаючи з PHP 7.1.0 і була *ВИДАЛЕНО* у версії PHP 7.2.0. Використовувати цю функцію не рекомендується.

### Опис

```methodsynopsis
mcrypt_list_algorithms(string $lib_dir = ini_get("mcrypt.algorithms_dir")): array
```

Отримати список усіх підтримуваних алгоритмів шифрування в заданій директорії `lib_dir`

### Список параметрів

`lib_dir`

Вказує директорію, де розташовані алгоритми. Якщо не встановлено, то буде використано значення директиви `mcrypt.algorithms_dir` із php.ini.

### Значення, що повертаються

Повертає масив алгоритмів, що підтримуються.

### Приклади

**Приклад #1 Приклад використання **mcryptlistalgorithms()****

```php
<?php
$algorithms = mcrypt_list_algorithms();
print_r($algorithms);
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
Array
(
    [0] => cast-128
    [1] => gost
    [2] => rijndael-128
    [3] => twofish
    [4] => arcfour
    [5] => cast-256
    [6] => loki97
    [7] => rijndael-192
    [8] => saferplus
    [9] => wake
    [10] => blowfish-compat
    [11] => des
    [12] => rijndael-256
    [13] => serpent
    [14] => xtea
    [15] => blowfish
    [16] => enigma
    [17] => rc2
    [18] => tripledes
)
```