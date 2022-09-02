---
navigation:
  - function.ps-curveto.md: «pscurveto
  - function.ps-end-page.md: псendpage »
  - index.md: PHP Manual
  - ref.ps.md: Функції PS
title: псdelete
---
# псdelete

(PECL ps >= 1.1.0)

псdelete — Видалення всіх ресурсів документа PostScript

### Опис

```methodsynopsis
ps_delete(resource $psdoc): bool
```

В основному звільняє пам'ять, що використовується документом. Також закриває файл, якщо він не був раніше закритий за допомогою [псclose()](function.ps-close.md). У будь-якому випадку вам слід закрити файл за допомогою [псclose()](function.ps-close.md) раніше, тому що [псclose()](function.ps-close.md) не лише закриває файл, але й виводить дані, що містять коментарі PostScript, такі як кількість сторінок у документі та додавання ієрархії закладок.

### Список параметрів

`psdoc`

Ідентифікатор ресурсу файлу postscript, повернутий [псnew()](function.ps-new.md)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [псclose()](function.ps-close.md) - Закриває документ PostScript
