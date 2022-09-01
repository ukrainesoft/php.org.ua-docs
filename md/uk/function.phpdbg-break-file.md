---
navigation:
  - ref.phpdbg.md: « Функции phpdbg
  - function.phpdbg-break-function.html: phpdbgbreakfunction »
  - index.md: PHP Manual
  - ref.phpdbg.md: Функции phpdbg
title: phpdbgbreakfile
---
# phpdbgbreakfile

(PHP 5> = 5.6.3, PHP 7, PHP 8)

phpdbgbreakfile — Додати точку переривання на конкретний рядок файлу

### Опис

```methodsynopsis
phpdbg_break_file(string $file, int $line): void
```

Додає точку переривання на рядок `line` файлу `file`

### Список параметрів

`file`

Ім'я файлу.

`line`

Номер рядка.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Дивіться також

-   [phpdbgbreakfunction()](function.phpdbg-break-function.html) - Додати точку переривання на виклик функції
-   [phpdbgbreakmethod()](function.phpdbg-break-method.html) - Додати точку переривання на виклик методу класу
-   [phpdbgbreaknext()](function.phpdbg-break-next.html) - Додати точку переривання на наступний опкод
-   [phpdbgclear()](function.phpdbg-clear.html) - Прибрати всі точки переривання
