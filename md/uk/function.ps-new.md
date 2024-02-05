---
navigation:
  - function.ps-moveto.md: « ps\_moveto
  - function.ps-open-file.md: ps\_open\_file »
  - index.md: PHP Manual
  - ref.ps.md: Функції PS
title: ps\_new
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ps\_new

(PECL ps >= 1.1.0)

ps\_new — Створює новий об'єкт документа PostScript

### Опис

```methodsynopsis
ps_new(): resource|false
```

Створює новий екземпляр документа. Функція не створює файл на диску чи пам'яті, вона просто все налаштовує. За **ps\_new()** зазвичай слідує виклик [ps\_open\_file()](function.ps-open-file.md) для фактичного створення документа postscript.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Ресурс документа PostScript или\*\*`false`\*\* у разі виникнення помилки. Значення, що повертається, передається всім іншим функціям як перший аргумент.

### Дивіться також

-   [ps\_delete()](function.ps-delete.md) \- Видаляє всі ресурси документа PostScript
