Спробувати задати контекст виконання

-   [« phpdbgendoplog](function.phpdbg-end-oplog.html)
    
-   [phpdbggetexecutable »](function.phpdbg-get-executable.html)
    
-   [PHP Manual](index.md)
    
-   [Функции phpdbg](ref.phpdbg.md)
    
-   Спробувати задати контекст виконання
    

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