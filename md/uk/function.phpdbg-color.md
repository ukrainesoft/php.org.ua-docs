---
navigation:
  - function.phpdbg-clear.md: « phpdbgclear
  - function.phpdbg-end-oplog.md: phpdbgendoplog »
  - index.md: PHP Manual
  - ref.phpdbg.md: Функции phpdbg
title: phpdbgcolor
---
# phpdbgcolor

(PHP 5> = 5.6.0, PHP 7, PHP 8)

phpdbgcolor — Задати колір елементу

### Опис

```methodsynopsis
phpdbg_color(int $element, string $color): void
```

Встановлює колір `color` для елемента `element`

### Список параметрів

`element`

Одна з констант **`PHPDBG_COLOR_*`**

`color`

Назва кольору. Одне з: `white` `red` `green` `yellow` `blue` `purple` `cyan` або `black`. Опціонально можна використовувати суфікси `-bold` або `-underline`. Наприклад `white-bold` або `green-underline`

### Значення, що повертаються

Функція не повертає значення після виконання.

### Дивіться також

-   [phpdbgprompt()](function.phpdbg-prompt.md) - встановити запрошення командного рядка
