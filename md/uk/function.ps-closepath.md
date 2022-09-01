---
navigation:
  - function.ps-closepath-stroke.html: «psclosepathstroke
  - function.ps-continue-text.html: псcontinuetext »
  - index.md: PHP Manual
  - ref.ps.md: Функції PS
title: псclosepath
---
# псclosepath

(PECL ps >= 1.1.0)

псclosepath - Замикає шлях

### Опис

```methodsynopsis
ps_closepath(resource $psdoc): bool
```

Поєднує останню точку з першою точкою шляху. Отриманий контур можна використовувати для обведення, заливки, обрізки тощо.

### Список параметрів

`psdoc`

Ідентифікатор ресурсу файлу postscript, повернутий функцією [псnew()](function.ps-new.md)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [псclip()](function.ps-clip.md) - Відображення кліпів по поточному шляху
-   [псclosepathstroke()](function.ps-closepath-stroke.md) - Замикає та обводить контур
