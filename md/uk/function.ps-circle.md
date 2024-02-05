---
navigation:
  - function.ps-begin-template.md: « ps\_begin\_template
  - function.ps-clip.md: ps\_clip »
  - index.md: PHP Manual
  - ref.ps.md: Функції PS
title: ps\_circle
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ps\_circle

(PECL ps >= 1.1.0)

ps\_circle — Малює коло

### Опис

```methodsynopsis
ps_circle(    resource $psdoc,    float $x,    float $y,    float $radius): bool
```

Малює коло із середньою точкою в точці (`x` `y`). Коло починається і закінчується в позиції (`x`\+ `radius` `y`). Якщо функція викликається поза дорогою, вона розпочне новий шлях. Якщо функція викликається всередині шляху, вона додасть коло як дочірній шлях. Якщо остання операція малювання не закінчується точкою (`x`\+ `radius` `y`), тоді на шляху буде розрив.

### Список параметрів

`psdoc`

Ідентифікатор ресурсу файлу postscript, повернутий функцією [ps\_new()](function.ps-new.md)

`x`

Координата X центру кола.

`y`

Координати центру кола Y.

`radius`

Радіус кола.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   [ps\_arc()](function.ps-arc.md) \- Малює дугу проти годинникової стрілки
-   [ps\_arcn()](function.ps-arcn.md) \- Малює дугу за годинниковою стрілкою
