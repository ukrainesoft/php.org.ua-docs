---
navigation:
  - function.phpdbg-break-file.md: « phpdbg\_break\_file
  - function.phpdbg-break-method.md: phpdbg\_break\_method »
  - index.md: PHP Manual
  - ref.phpdbg.md: Функції phpdbg
title: phpdbg\_break\_function
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# phpdbg\_break\_function

(PHP 5 >= 5.6.3, PHP 7, PHP 8)

phpdbg\_break\_function — Додати точку переривання на дзвінок функції

### Опис

```methodsynopsis
phpdbg_break_function(string $function): void
```

Додає точку переривання на дзвінок функції `function`

### Список параметрів

`function`

Ім'я функції.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Дивіться також

-   [phpdbg\_break\_file()](function.phpdbg-break-file.md) \- Додати точку переривання на конкретний рядок файлу
-   [phpdbg\_break\_method()](function.phpdbg-break-method.md) \- Додати точку переривання на виклик методу класу
-   [phpdbg\_break\_next()](function.phpdbg-break-next.md) \- Додати точку переривання на наступний опкод
-   [phpdbg\_clear()](function.phpdbg-clear.md) \- Прибрати всі точки переривання
