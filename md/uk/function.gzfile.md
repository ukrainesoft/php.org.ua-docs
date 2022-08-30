Зчитує весь gz-файл у масив

-   [« gzeof](function.gzeof.html)
    
-   [gzgetc »](function.gzgetc.html)
    
-   [PHP Manual](index.html)
    
-   [Функции Zlib](ref.zlib.html)
    
-   Зчитує весь gz-файл у масив
    

# gzfile

(PHP 4, PHP 5, PHP 7, PHP 8)

gzfile — Зчитує весь gz-файл у масив

### Опис

```methodsynopsis
gzfile(string $filename, int $use_include_path = 0): array|false
```

Аналогічна [readgzfile()](function.readgzfile.html), За винятком того, що вона повертає файл у масиві.

### Список параметрів

`filename`

Ім'я файлу.

`use_include_path`

Якщо ви хочете, щоб також перевірялася наявність файлу в директоріях [includepath](ini.core.html#ini.include-path), встановіть значення цього параметра в `1`

### Значення, що повертаються

Масив рядків файлу, у кожному елементі масиву знаходиться один рядок, порожні рядки включаються, а перенесення рядків, як і раніше, додаються або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **gzfile()****

```php
<?php
$lines = gzfile('somefile.gz');
foreach ($lines as $line) {
    echo $line;
}
?>
```

### Дивіться також

-   [readgzfile()](function.readgzfile.html) - Виводить вміст gz-файлу
-   [gzopen()](function.gzopen.html) - Відкрити gz-файл