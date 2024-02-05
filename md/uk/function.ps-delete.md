---
navigation:
  - function.ps-curveto.md: « ps\_curveto
  - function.ps-end-page.md: ps\_end\_page »
  - index.md: PHP Manual
  - ref.ps.md: Функції PS
title: ps\_delete
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ps\_delete

(PECL ps >= 1.1.0)

ps\_delete — Видалення всіх ресурсів документа PostScript

### Опис

```methodsynopsis
ps_delete(resource $psdoc): bool
```

В основному звільняє пам'ять, що використовується документом. Також закриває файл, якщо він не був раніше закритий за допомогою [ps\_close()](function.ps-close.md). У будь-якому випадку вам слід закрити файл за допомогою [ps\_close()](function.ps-close.md) раніше, тому що [ps\_close()](function.ps-close.md) не тільки закриває файл, але й виводить дані, що містять коментарі PostScript, такі як кількість сторінок у документі та додавання ієрархії закладок.

### Список параметрів

`psdoc`

Ідентифікатор ресурсу файлу postscript, повернутий [ps\_new()](function.ps-new.md)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   [ps\_close()](function.ps-close.md) \- Закриває документ PostScript
