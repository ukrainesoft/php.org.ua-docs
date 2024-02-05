---
navigation:
  - function.ps-close-image.md: « ps\_close\_image
  - function.ps-closepath-stroke.md: ps\_closepath\_stroke »
  - index.md: PHP Manual
  - ref.ps.md: Функції PS
title: ps\_close
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ps\_close

(PECL ps >= 1.1.0)

ps\_close — Закриває документ PostScript

### Опис

```methodsynopsis
ps_close(resource $psdoc): bool
```

Закриває документ PostScript.

Функція записує кількість сторінок у документі PostScript. Вона також записує ієрархію закладок . **ps\_close()** не звільняє ресурси, як [ps\_delete()](function.ps-delete.md)

Функція також викликається функцією [ps\_delete()](function.ps-delete.md)якщо вона не була викликана раніше.

### Список параметрів

`psdoc`

Ідентифікатор ресурсу файлу postscript, повернутий функцією [ps\_new()](function.ps-new.md)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   [ps\_open\_file()](function.ps-open-file.md) \- Відкриває файл для виводу
-   [ps\_delete()](function.ps-delete.md) \- Видаляє всі ресурси документа PostScript
