Отримати символ із покажчика на gz-файл

-   [« gzfile](function.gzfile.html)
    
-   [gzgets »](function.gzgets.html)
    
-   [PHP Manual](index.html)
    
-   [Функции Zlib](ref.zlib.html)
    
-   Отримати символ із покажчика на gz-файл
    

# gzgetc

(PHP 4, PHP 5, PHP 7, PHP 8)

gzgetc — Отримати символ із покажчика на gz-файл

### Опис

```methodsynopsis
gzgetc(resource $stream): string|false
```

Повертає рядок, що містить один символ (несжатий), зчитаний із заданого покажчика gz-файлу.

### Список параметрів

`stream`

Вказівник на файл gz. Він має бути коректним і повинен вказувати на файл, успішно відкритий. [gzopen()](function.gzopen.html)

### Значення, що повертаються

Символ (несжатий) або **`false`** у випадку EOF (на відміну від [gzeof()](function.gzeof.html)

### Приклади

**Приклад #1 Приклад використання **gzgetc()****

```php
<?php
$gz = gzopen('somefile.gz', 'r');
while (!gzeof($gz)) {
  echo gzgetc($gz);
}
gzclose($gz);
?>
```

### Дивіться також

-   [gzopen()](function.gzopen.html) - Відкрити gz-файл
-   [gzgets()](function.gzgets.html) - Отримати рядок із покажчика файлу