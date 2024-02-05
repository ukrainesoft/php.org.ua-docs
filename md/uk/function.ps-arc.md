---
navigation:
  - function.ps-add-weblink.md: « ps\_add\_weblink
  - function.ps-arcn.md: ps\_arcn »
  - index.md: PHP Manual
  - ref.ps.md: Функції PS
title: ps\_arc
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ps\_arc

(PECL ps >= 1.1.0)

ps\_arc — Малює дугу проти годинникової стрілки.

### Опис

```methodsynopsis
ps_arc(    resource $psdoc,    float $x,    float $y,    float $radius,    float $alpha,    float $beta): bool
```

Малює частину кола із середньою точкою в точці (`x` `y`). Дуга начинается под углом`alpha` і закінчується під кутом `beta`. Вона малюється проти годинникової стрілки (використовуйте [ps\_arcn()](function.ps-arcn.md) для малювання за годинниковою стрілкою). Дочірній шлях, доданий до поточного шляху, починається на дузі під кутом `alpha` і закінчується на дузі під кутом `beta`

### Список параметрів

`psdoc`

Ідентифікатор ресурсу файлу postscript, повернутий функцією [ps\_new()](function.ps-new.md)

`x`

Координата X середньої точки кола.

`y`

Координата Y середньої точки кола.

`radius`

Радіус кола.

`alpha`

Початковий кут у градусах.

`beta`

Кінцевий кут у градусах.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   [ps\_arcn()](function.ps-arcn.md) \- Малює дугу за годинниковою стрілкою
