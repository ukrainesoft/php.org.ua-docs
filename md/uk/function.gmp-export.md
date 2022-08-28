Експортувати в бінарний рядок

-   [« gmp\_divexact](function.gmp-divexact.html)
    
-   [gmp\_fact »](function.gmp-fact.html)
    
-   [PHP Manual](index.html)
    
-   [GMP Функции](ref.gmp.html)
    
-   Експортувати в бінарний рядок
    

# gmpexport

(PHP 5> = 5.6.1, PHP 7, PHP 8)

gmpexport — Експортувати до бінарного рядка

### Опис

```methodsynopsis
gmp_export(GMP|int|string $num, int $word_size = 1, int $flags = GMP_MSW_FIRST | GMP_NATIVE_ENDIAN): string
```

Експортує GMP-число до бінарного рядка

### Список параметрів

`num`

GMP-число для експорту

`word_size`

За замовчуванням дорівнює 1. Кількість байт у кожному блоці бінарних даних. Зазвичай використовується разом із завданням options.

`flags`

За замовчуванням **`GMP_MSW_FIRST`** **`GMP_NATIVE_ENDIAN`**

### Значення, що повертаються

Повертає рядок.

### список змін

| Версия | Описание                                                          |
|--------|-------------------------------------------------------------------|
|        | Функція більше не повертає **`false`** у разі виникнення помилки. |

### Приклади

**Приклад #1 Приклад використання **gmpexport()****

```php
<?php
$number = gmp_init(16705);
echo gmp_export($number) . "\n";
?>
```

Результат виконання цього прикладу:

```
AA
```

### Дивіться також

-   [gmp\_import()](function.gmp-import.html) - Імпортувати з бінарного рядка