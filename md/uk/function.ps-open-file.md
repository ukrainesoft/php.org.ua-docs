---
navigation:
  - function.ps-new.md: «psnew
  - function.ps-open-image-file.md: псopenimagefile »
  - index.md: PHP Manual
  - ref.ps.md: Функції PS
title: псopenfile
---
# псopenfile

(PECL ps >= 1.1.0)

псopenfile — Відкриває файл для виводу

### Опис

```methodsynopsis
ps_open_file(resource $psdoc, string $filename = ?): bool
```

Створює новий файл на диску і записує документ PostScript. Файл буде закрито під час виклику [псclose()](function.ps-close.md)

### Список параметрів

`psdoc`

Ідентифікатор ресурсу файлу postscript, повернутий [псnew()](function.ps-new.md)

`filename`

Назва файлу postscript. Якщо `filename` не передано, документ буде створено в пам'яті і весь висновок йтиме прямо до браузера.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [псclose()](function.ps-close.md) - Закриває документ PostScript
