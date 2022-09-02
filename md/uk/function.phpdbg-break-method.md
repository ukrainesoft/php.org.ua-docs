---
navigation:
  - function.phpdbg-break-function.md: « phpdbgbreakfunction
  - function.phpdbg-break-next.md: phpdbgbreaknext »
  - index.md: PHP Manual
  - ref.phpdbg.md: Функции phpdbg
title: phpdbgbreakметод
---
# phpdbgbreakметод

(PHP 5> = 5.6.3, PHP 7, PHP 8)

phpdbgbreakmethod — Додати точку переривання на виклик методу класу

### Опис

```methodsynopsis
phpdbg_break_method(string $class, string $method): void
```

Додає точку переривання на виклик методу `method` класу `class`

### Список параметрів

`class`

Назва класу.

`method`

Ім'я методу.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Дивіться також

-   [phpdbgbreakfile()](function.phpdbg-break-file.md) - Додати точку переривання на конкретний рядок файлу
-   [phpdbgbreakfunction()](function.phpdbg-break-function.md) - Додати точку переривання на виклик функції
-   [phpdbgbreaknext()](function.phpdbg-break-next.md) - Додати точку переривання на наступний опкод
-   [phpdbgclear()](function.phpdbg-clear.md) - Прибрати всі точки переривання
