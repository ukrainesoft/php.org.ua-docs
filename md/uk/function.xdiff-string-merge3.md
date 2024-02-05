---
navigation:
  - function.xdiff-string-diff.md: « xdiff\_string\_diff
  - function.xdiff-string-patch-binary.md: xdiff\_string\_patch\_binary »
  - index.md: PHP Manual
  - ref.xdiff.md: Функції xdiff
title: xdiff\_string\_merge3
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# xdiff\_string\_merge3

(PECL xdiff >= 0.2.0)

xdiff\_string\_merge3 — Об'єднати три рядки в один

### Опис

```methodsynopsis
xdiff_string_merge3(    string $old_data,    string $new_data1,    string $new_data2,    string &$error = ?): mixed
```

Поєднує три рядки в один і повертає результат. У параметрі `old_data` задається оригінальний рядок, а в `new_data1`и`new_data2` - Її модифіковані версії. Опціональний параметр `error` використовується для збереження помилок у процесі об'єднання.

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

Повертає отриманий рядок, **`false`**в случае возникновения ошибки или**`true`**, якщо отриманий рядок порожній.

### Дивіться також

-   [xdiff\_file\_merge3()](function.xdiff-file-merge3.md) \- Об'єднання трьох файлів в один
