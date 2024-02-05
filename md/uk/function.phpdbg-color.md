---
navigation:
  - function.phpdbg-clear.md: « phpdbg\_clear
  - function.phpdbg-end-oplog.md: phpdbg\_end\_oplog »
  - index.md: PHP Manual
  - ref.phpdbg.md: Функції phpdbg
title: phpdbg\_color
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# phpdbg\_color

(PHP 5 >= 5.6.0, PHP 7, PHP 8)

phpdbg\_color — Задати колір елементу

### Опис

```methodsynopsis
phpdbg_color(int $element, string $color): void
```

Устанавливает цвет`color` для елемента `element`

### Список параметрів

`element`

Одна из констант\*\*`PHPDBG_COLOR_*`\*\*

`color`

Имя цвета. Одно из:`white` `red` `green` `yellow` `blue` `purple` `cyan`или`black`. Опціонально можна використовувати суфікси `-bold`или`-underline`К примеру`white-bold`или`green-underline`

### Значення, що повертаються

Функція не повертає значення після виконання.

### Дивіться також

-   [phpdbg\_prompt()](function.phpdbg-prompt.md) \- встановити запрошення командного рядка
