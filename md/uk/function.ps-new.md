---
navigation:
  - function.ps-moveto.html: «psmoveto
  - function.ps-open-file.html: псopenfile »
  - index.md: PHP Manual
  - ref.ps.md: Функції PS
title: псnew
---
# псnew

(PECL ps >= 1.1.0)

псnew — Створює новий об'єкт документа PostScript

### Опис

```methodsynopsis
ps_new(): resource|false
```

Створює новий екземпляр документа. Функція не створює файл на диску чи пам'яті, вона просто все налаштовує. За **псnew()** зазвичай слідує виклик [псopenfile()](function.ps-open-file.html) для фактичного створення документа postscript.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Ресурс документа PostScript або **`false`** у разі виникнення помилки. Значення, що повертається, передається всім іншим функціям як перший аргумент.

### Дивіться також

-   [псdelete()](function.ps-delete.html) - Видаляє всі ресурси документа PostScript
