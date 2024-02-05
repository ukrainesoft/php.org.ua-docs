---
navigation:
  - ref.phpdbg.md: « Функції phpdbg
  - function.phpdbg-break-function.md: phpdbg\_break\_function »
  - index.md: PHP Manual
  - ref.phpdbg.md: Функції phpdbg
title: phpdbg\_break\_file
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# phpdbg\_break\_file

(PHP 5 >= 5.6.3, PHP 7, PHP 8)

phpdbg\_break\_file — Додати точку переривання на конкретний рядок файлу

### Опис

```methodsynopsis
phpdbg_break_file(string $file, int $line): void
```

Додає точку переривання на рядок `line`файла`file`

### Список параметрів

`file`

Ім'я файлу.

`line`

Номер рядка.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Дивіться також

-   [phpdbg\_break\_function()](function.phpdbg-break-function.md) \- Додати точку переривання на виклик функції
-   [phpdbg\_break\_method()](function.phpdbg-break-method.md) \- Додати точку переривання на виклик методу класу
-   [phpdbg\_break\_next()](function.phpdbg-break-next.md) \- Додати точку переривання на наступний опкод
-   [phpdbg\_clear()](function.phpdbg-clear.md) \- Прибрати всі точки переривання
