---
navigation:
  - function.phpdbg-end-oplog.md: « phpdbg\_end\_oplog
  - function.phpdbg-get-executable.md: phpdbg\_get\_executable »
  - index.md: PHP Manual
  - ref.phpdbg.md: Функції phpdbg
title: phpdbg\_exec
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# phpdbg\_exec

(PHP 5 >= 5.6.0, PHP 7, PHP 8)

phpdbg\_exec — Спробувати встановити контекст виконання

### Опис

```methodsynopsis
phpdbg_exec(string $context): string|bool
```

**Увага**

Функція поки що не документована; для знайомства доступний лише перелік аргументів.

### Список параметрів

`context`

### Значення, що повертаються

Попередній контекст виконання, якщо він був заданий . \*\*`true`\*\*якщо контекст виконання раніше не був заданий. Якщо запит на встановлення контексту завершиться з помилкою, то буде повернено **`false`** та викликана помилка рівня **`E_WARNING`**
