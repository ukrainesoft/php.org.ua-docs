---
navigation:
  - function.phpdbg-end-oplog.md: « phpdbgendoplog
  - function.phpdbg-get-executable.md: phpdbggetexecutable »
  - index.md: PHP Manual
  - ref.phpdbg.md: Функции phpdbg
title: phpdbgexec
---
# phpdbgexec

(PHP 5> = 5.6.0, PHP 7, PHP 8)

phpdbgexec — Спробувати встановити контекст виконання

### Опис

```methodsynopsis
phpdbg_exec(string $context): string|bool
```

**Увага**

На цей час ця функція ще була документована; для ознайомлення доступний лише перелік аргументів.

### Список параметрів

`context`

### Значення, що повертаються

Попередній контекст виконання, якщо він був заданий . \*\*`true`\*\*якщо контекст виконання раніше не був заданий. Якщо запит на встановлення контексту завершиться з помилкою, то буде повернено **`false`** та викликана помилка рівня **`E_WARNING`**
