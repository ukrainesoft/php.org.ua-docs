---
navigation:
  - ref.wddx.md: « Функції WDDX
  - function.wddx-deserialize.md: wddx\_deserialize »
  - index.md: PHP Manual
  - ref.wddx.md: Функції WDDX
title: wddx\_add\_vars
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# wddx\_add\_vars

(PHP 4, PHP 5, PHP 7)

wddx\_add\_vars — Додати змінні до пакету WDDX із зазначеним ідентифікатором

**Увага**

Ця функція була *ВИДАЛЕНО* у PHP 7.4.0.

### Опис

```methodsynopsis
wddx_add_vars(resource $packet_id, mixed $var_name, mixed ...$var_names): bool
```

Серіалізує передані змінні та додає результат до цього пакету.

### Список параметрів

Функція приймає змінну кількість параметрів.

`packet_id`

Пакет WDDX, що повертається [wddx\_packet\_start()](function.wddx-packet-start.md)

`var_name`

Може бути або рядком, що означає змінну, або масивом, що містить рядки з іменами змінних або інші масиви і т.д.

`var_names`

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.
