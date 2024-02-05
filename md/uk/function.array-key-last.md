---
navigation:
  - function.array-key-first.md: « array\_key\_first
  - function.array-keys.md: array\_keys »
  - index.md: PHP Manual
  - ref.array.md: Функції для роботи з масивами
title: array\_key\_last
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# array\_key\_last

(PHP 7 >= 7.3.0, PHP 8)

array\_key\_last — Отримує останній ключ масиву

### Опис

```methodsynopsis
array_key_last(array $array): int|string|null
```

Получить последний ключ заданного массива`array`, не торкаючись внутрішнього покажчика масиву.

### Список параметрів

`array`

Масив.

### Значення, що повертаються

Повертає останній ключ масиву `array`якщо він не порожній; **`null`** в іншому випадку.

### Дивіться також

-   [array\_key\_first()](function.array-key-first.md) \- Отримує перший ключ масиву
-   [end()](function.end.md) - Встановлює внутрішній покажчик масиву на останній елемент
