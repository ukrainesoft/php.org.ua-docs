---
navigation:
  - function.phpdbg-break-next.md: « phpdbg\_break\_next
  - function.phpdbg-color.md: phpdbg\_color »
  - index.md: PHP Manual
  - ref.phpdbg.md: Функції phpdbg
title: phpdbg\_clear
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# phpdbg\_clear

(PHP 5 >= 5.6.0, PHP 7, PHP 8)

phpdbg\_clear — Видалити всі точки переривання

### Опис

```methodsynopsis
phpdbg_clear(): void
```

Видаляє всі задані раніше точки переривання. Працює як для заданих за допомогою функцій **phpdbg\_break\_\*()**, і для доданих вручну через консоль.

**Увага**

Функція поки що не документована; для знайомства доступний лише перелік аргументів.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Дивіться також

-   [phpdbg\_break\_file()](function.phpdbg-break-file.md) \- Додати точку переривання на конкретний рядок файлу
-   [phpdbg\_break\_function()](function.phpdbg-break-function.md) \- Додати точку переривання на виклик функції
-   [phpdbg\_break\_method()](function.phpdbg-break-method.md) \- Додати точку переривання на виклик методу класу
-   [phpdbg\_break\_next()](function.phpdbg-break-next.md) \- Додати точку переривання на наступний опкод
