---
navigation:
  - function.sleep.md: « sleep
  - function.time-nanosleep.md: time\_nanosleep »
  - index.md: PHP Manual
  - ref.misc.md: Різні функції
title: sys\_getloadavg
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# sys\_getloadavg

(PHP 5 >= 5.1.3, PHP 7, PHP 8)

sys\_getloadavg — Отримує середнє завантаження системи

### Опис

```methodsynopsis
sys_getloadavg(): array|false
```

Повертає три зразки, що представляють середнє завантаження системи (кількість процесів у черзі системних процесів) за останні 1, 5 і 15 хвилин, відповідно. Повертає \*\*`false`\*\*в случае возникновения ошибки.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає масив (array) із трьома зразками (останні 1, 5 та 15 хвилин).

### Приклади

**Приклад #1 Приклад використання** sys\_getloadavg()\*\*\*\*

```php
<?php
$load = sys_getloadavg();
if ($load[0] > 0.80) {
    header('HTTP/1.1 503 Too busy, try again later');
    die('Server too busy. Please try again later.');
}
?>
```

### Примітки

> **Зауваження**: Для Windows-платформ ця функція не реалізована.
