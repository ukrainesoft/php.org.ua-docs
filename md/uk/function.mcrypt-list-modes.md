Отримати список усіх підтримуваних режимів шифрування

-   [« mcrypt\_list\_algorithms](function.mcrypt-list-algorithms.html)
    
-   [mcrypt\_module\_close »](function.mcrypt-module-close.html)
    
-   [PHP Manual](index.html)
    
-   [Mcrypt](ref.mcrypt.html)
    
-   Отримати список усіх підтримуваних режимів шифрування
    

# mcryptlistmodes

(PHP 4 >= 4.0.2, PHP 5, PHP 7 < 7.2.0, PECL mcrypt >= 1.0.0)

mcryptlistmodes — Отримати список усіх підтримуваних режимів шифрування

**Увага**

Ця функція оголошена *Застарілої*, починаючи з PHP 7.1.0 і була *ВИДАЛЕНО* у версії PHP 7.2.0. Використовувати цю функцію не рекомендується.

### Опис

```methodsynopsis
mcrypt_list_modes(string $lib_dir = ini_get("mcrypt.modes_dir")): array
```

Отримати список усіх режимів шифрування з директорії `lib_dir`

### Список параметрів

`lib_dir`

Вказує директорію, де розташовані режими. Якщо не встановлено, то буде використано значення директиви `mcrypt.modes_dir` із php.ini.

### Значення, що повертаються

Повертає масив підтримуваних режимів.

### Приклади

**Приклад #1 Приклад використання **mcryptlistmodes()****

```php
<?php
    $modes = mcrypt_list_modes();

    foreach ($modes as $mode) {
        echo "$mode <br />\n";
    }
?>
```

Приклад вище демонструє отримання списку всіх алгоритмів директорії за замовчуванням. Якщо директива php.ini `mcrypt.modes_dir` не задана, буде використана директорія mcrypt за замовчуванням (/usr/local/lib/libmcrypt).