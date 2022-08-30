Імпортувати з бінарного рядка

-   [« gmphamdist](function.gmp-hamdist.html)
    
-   [gmpinit »](function.gmp-init.html)
    
-   [PHP Manual](index.html)
    
-   [GMP Функції](ref.gmp.html)
    
-   Імпортувати з бінарного рядка
    

# gmpimport

(PHP 5> = 5.6.1, PHP 7, PHP 8)

gmpimport — Імпортувати з бінарного рядка

### Опис

```methodsynopsis
gmp_import(string $data, int $word_size = 1, int $flags = GMP_MSW_FIRST | GMP_NATIVE_ENDIAN): GMP
```

Імпортує GMP-число з бінарного рядка

### Список параметрів

`data`

Бінарний рядок для імпорту

`word_size`

За замовчуванням дорівнює 1. Кількість байт у кожному блоці бінарних даних. Зазвичай використовується разом із завданням options.

`flags`

За замовчуванням **`GMP_MSW_FIRST`** **`GMP_NATIVE_ENDIAN`**

### Значення, що повертаються

Повертає GMP-число.

### список змін

| Версия | Описание                                                          |
|--------|-------------------------------------------------------------------|
|        | Функція більше не повертає **`false`** у разі виникнення помилки. |

### Приклади

**Приклад #1 Приклад використання **gmpimport()****

```php
<?php
$number = gmp_import("\0");
echo gmp_strval($number) . "\n";

$number = gmp_import("\0\1\2");
echo gmp_strval($number) . "\n";
?>
```

Результат виконання цього прикладу:

```
0
258
```

### Дивіться також

-   [gmpexport()](function.gmp-export.html) - Експортувати у бінарний рядок