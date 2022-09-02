---
navigation:
  - function.array-key-first.md: « arraykeyfirst
  - function.array-keys.md: arraykeys »
  - index.md: PHP Manual
  - ref.array.md: Функції для роботи з масивами
title: arraykeylast
---
# arraykeylast

(PHP 7> = 7.3.0, PHP 8)

arraykeylast — Отримує останній ключ масиву

### Опис

```methodsynopsis
array_key_last(array $array): int|string|null
```

Отримати останній ключ заданого масиву `array`, не торкаючись внутрішнього покажчика масиву.

### Список параметрів

`array`

Масив.

### Значення, що повертаються

Повертає останній ключ масиву `array`якщо він не порожній; **`null`** в іншому випадку.

### Дивіться також

-   [arraykeyfirst()](function.array-key-first.md) - Отримує перший ключ масиву
-   [end()](function.end.md) - Встановлює внутрішній покажчик масиву на його останній елемент
