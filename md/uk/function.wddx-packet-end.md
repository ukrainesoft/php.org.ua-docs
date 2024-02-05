---
navigation:
  - function.wddx-deserialize.md: « wddx\_deserialize
  - function.wddx-packet-start.md: wddx\_packet\_start »
  - index.md: PHP Manual
  - ref.wddx.md: Функції WDDX
title: wddx\_packet\_end
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# wddx\_packet\_end

(PHP 4, PHP 5, PHP 7)

wddx\_packet\_end — Завершує пакет WDDX із зазначеним ідентифікатором

**Увага**

Ця функція була *ВИДАЛЕНО* у PHP 7.4.0.

### Опис

```methodsynopsis
wddx_packet_end(resource $packet_id): string
```

Завершує та повертає заданий пакет WDDX.

### Список параметрів

`packet_id`

Пакет WDDX, що повертається [wddx\_packet\_start()](function.wddx-packet-start.md)

### Значення, що повертаються

Повертає рядок, який містить пакет WDDX.
