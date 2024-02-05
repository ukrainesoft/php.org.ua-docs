---
navigation:
  - function.ps-makespotcolor.md: « ps\_makespotcolor
  - function.ps-new.md: ps\_new »
  - index.md: PHP Manual
  - ref.ps.md: Функції PS
title: ps\_moveto
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ps\_moveto

(PECL ps >= 1.1.0)

ps\_moveto — Встановлює поточну точку.

### Опис

```methodsynopsis
ps_moveto(resource $psdoc, float $x, float $y): bool
```

Встановлює нові координати поточної точки. Якщо це перший виклик **ps\_moveto()** після того, як попередній шлях було завершено, тоді функція запустить новий шлях. Якщо функція викликається всередині шляху, вона просто встановлює поточну точку та запускає додатковий шлях.

### Список параметрів

`psdoc`

Ідентифікатор ресурсу файлу postscript, повернутий [ps\_new()](function.ps-new.md)

`x`

Координата X точки, яку потрібно переміститися.

`y`

Координата Y точки, яку потрібно переміститися.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   [ps\_lineto()](function.ps-lineto.md) \- Малює лінію
