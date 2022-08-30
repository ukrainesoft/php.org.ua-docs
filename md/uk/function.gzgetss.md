Повертає рядок із покажчика gz-файлу та видалити HTML-теги

-   [« gzgets](function.gzgets.html)
    
-   [gzinflate »](function.gzinflate.html)
    
-   [PHP Manual](index.html)
    
-   [Функции Zlib](ref.zlib.html)
    
-   Повертає рядок із покажчика gz-файлу та видалити HTML-теги
    

# gzgetss

(PHP 4, PHP 5, PHP 7)

gzgetss — Повертає рядок із покажчика gz-файлу та видалити HTML-теги

**Увага**

Ця функція оголошена *застарілої*, починаючи з PHP 7.3.0 і була *ВИДАЛЕНО* у версії PHP 8.0.0. Використовувати цю функцію не рекомендується.

### Опис

```methodsynopsis
gzgetss(resource $zp, int $length, string $allowable_tags = ?): string
```

Аналогічно [gzgets()](function.gzgets.html), за винятком того, що **gzgetss()** намагається видалити будь-які теги HTML і PHP з рядка, що зчитується.

### Список параметрів

`zp`

Вказівник на файл gz. Він має бути коректним і повинен вказувати на файл, успішно відкритий. [gzopen()](function.gzopen.html)

`length`

Максимальний розмір даних, що повертаються.

`allowable_tags`

Використовуйте цей параметр, щоб вказати теги, які не потрібно видаляти.

### Значення, що повертаються

Нестиснений очищений рядок або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **gzgetss()****

```php
<?php
$handle = gzopen('somefile.gz', 'r');
while (!gzeof($handle)) {
   $buffer = gzgetss($handle, 4096);
   echo $buffer;
}
gzclose($handle);
?>
```

### Дивіться також

-   [gzopen()](function.gzopen.html) - Відкрити gz-файл
-   [gzgets()](function.gzgets.html) - Отримати рядок із покажчика файлу
-   [striptags()](function.strip-tags.html) - Видаляє теги HTML та PHP з рядка