---
navigation:
  - function.ps-new.md: « ps\_new
  - function.ps-open-image-file.md: ps\_open\_image\_file »
  - index.md: PHP Manual
  - ref.ps.md: Функції PS
title: ps\_open\_file
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ps\_open\_file

(PECL ps >= 1.1.0)

ps\_open\_file — Відкриває файл для виводу

### Опис

```methodsynopsis
ps_open_file(resource $psdoc, string $filename = ?): bool
```

Створює новий файл на диску і записує документ PostScript. Файл буде закрито під час виклику [ps\_close()](function.ps-close.md)

### Список параметрів

`psdoc`

Ідентифікатор ресурсу файлу postscript, повернутий [ps\_new()](function.ps-new.md)

`filename`

Имя файла postscript. Если`filename` не передано, документ буде створено в пам'яті і весь висновок йтиме прямо до браузера.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   [ps\_close()](function.ps-close.md) \- Закриває документ PostScript
