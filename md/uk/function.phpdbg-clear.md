---
navigation:
  - function.phpdbg-break-next.html: « phpdbgbreaknext
  - function.phpdbg-color.html: phpdbgcolor »
  - index.md: PHP Manual
  - ref.phpdbg.md: Функции phpdbg
title: phpdbgclear
---
# phpdbgclear

(PHP 5> = 5.6.0, PHP 7, PHP 8)

phpdbgclear — Видалити всі точки переривання

### Опис

```methodsynopsis
phpdbg_clear(): void
```

Видаляє всі задані раніше точки переривання. Працює як для заданих за допомогою функцій **phpdbgbreak**, і для доданих вручну через консоль.

**Увага**

На цей час ця функція ще була документована; для ознайомлення доступний лише перелік аргументів.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Дивіться також

-   [phpdbgbreakfile()](function.phpdbg-break-file.md) - Додати точку переривання на конкретний рядок файлу
-   [phpdbgbreakfunction()](function.phpdbg-break-function.md) - Додати точку переривання на виклик функції
-   [phpdbgbreakmethod()](function.phpdbg-break-method.md) - Додати точку переривання на виклик методу класу
-   [phpdbgbreaknext()](function.phpdbg-break-next.md) - Додати точку переривання на наступний опкод
