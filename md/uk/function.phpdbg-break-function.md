---
navigation:
  - function.phpdbg-break-file.html: « phpdbgbreakfile
  - function.phpdbg-break-method.html: phpdbgbreakmethod »
  - index.md: PHP Manual
  - ref.phpdbg.md: Функции phpdbg
title: phpdbgbreakfunction
---
# phpdbgbreakfunction

(PHP 5> = 5.6.3, PHP 7, PHP 8)

phpdbgbreakfunction — Додати точку переривання на дзвінок функції

### Опис

```methodsynopsis
phpdbg_break_function(string $function): void
```

Додає точку переривання на виклик функції `function`

### Список параметрів

`function`

Ім'я функції.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Дивіться також

-   [phpdbgbreakfile()](function.phpdbg-break-file.html) - Додати точку переривання на конкретний рядок файлу
-   [phpdbgbreakmethod()](function.phpdbg-break-method.html) - Додати точку переривання на виклик методу класу
-   [phpdbgbreaknext()](function.phpdbg-break-next.html) - Додати точку переривання на наступний опкод
-   [phpdbgclear()](function.phpdbg-clear.html) - Прибрати всі точки переривання
