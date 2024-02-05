---
navigation:
  - function.phpdbg-break-function.md: « phpdbg\_break\_function
  - function.phpdbg-break-next.md: phpdbg\_break\_next »
  - index.md: PHP Manual
  - ref.phpdbg.md: Функції phpdbg
title: phpdbg\_break\_method
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# phpdbg\_break\_method

(PHP 5 >= 5.6.3, PHP 7, PHP 8)

phpdbg\_break\_method — Додати точку переривання на виклик методу класу

### Опис

```methodsynopsis
phpdbg_break_method(string $class, string $method): void
```

Додає точку переривання на виклик методу `method`класса`class`

### Список параметрів

`class`

Назва класу.

`method`

Ім'я методу.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Дивіться також

-   [phpdbg\_break\_file()](function.phpdbg-break-file.md) \- Додати точку переривання на конкретний рядок файлу
-   [phpdbg\_break\_function()](function.phpdbg-break-function.md) \- Додати точку переривання на виклик функції
-   [phpdbg\_break\_next()](function.phpdbg-break-next.md) \- Додати точку переривання на наступний опкод
-   [phpdbg\_clear()](function.phpdbg-clear.md) \- Прибрати всі точки переривання
