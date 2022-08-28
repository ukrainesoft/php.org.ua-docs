Об'єднати три рядки в один

-   [« xdiff\_string\_diff](function.xdiff-string-diff.html)
    
-   [xdiff\_string\_patch\_binary »](function.xdiff-string-patch-binary.html)
    
-   [PHP Manual](index.html)
    
-   [Функции xdiff](ref.xdiff.html)
    
-   Об'єднати три рядки в один
    

# xdiffstringmerge3

(PECL xdiff >= 0.2.0)

xdiffstringmerge3 — Об'єднати три рядки в один

### Опис

```methodsynopsis
xdiff_string_merge3(    string $old_data,    string $new_data1,    string $new_data2,    string &$error = ?): mixed
```

Поєднує три рядки в один і повертає результат. У параметрі `old_data` задається оригінальний рядок, а в `new_data1` і `new_data2` - Її модифіковані версії. Опціональний параметр `error` використовується для збереження помилок у процесі об'єднання.

### Список параметрів

`old_data`

Перший рядок із даними. Це будуть "старі" дані.

`new_data1`

Другий рядок із даними. Модифікована версія `old_data`

`new_data2`

Третій рядок із даними. Модифікована версія `old_data`

`error`

Якщо заданий, то сюди записуватимуться помилки, що виникли.

### Значення, що повертаються

Повертає отриманий рядок, **`false`** у разі виникнення помилки або **`true`**, якщо отриманий рядок порожній.

### Дивіться також

-   [xdiff\_file\_merge3()](function.xdiff-file-merge3.html) - Об'єднання трьох файлів в один