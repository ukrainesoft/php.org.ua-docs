---
navigation:
  - function.wddx-add-vars.md: « wddx\_add\_vars
  - function.wddx-packet-end.md: wddx\_packet\_end »
  - index.md: PHP Manual
  - ref.wddx.md: Функції WDDX
title: wddx\_deserialize
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# wddx\_deserialize

(PHP 4, PHP 5, PHP 7)

wddx\_deserialize - Десеріалізує пакет WDDX

**Увага**

Ця функція була *ВИДАЛЕНО* у PHP 7.4.0.

### Опис

```methodsynopsis
wddx_deserialize(string $packet): mixed
```

Десериализует пакет`packet`WDDX.

**Увага**

Не передавайте неперевірене введення користувача в **wddx\_deserialize()**. Десеріалізація може призвести до того, що код завантажується і виконується під час ініціалізації та автозавантаження, і зловмисник може скористатися цим. Використовуйте безпечний стандартний формат обміну даними, таким як JSON (через [json\_decode()](function.json-decode.md) і [json\_encode()](function.json-encode.md)), якщо вам необхідно передати серіалізовані дані користувачеві.

### Список параметрів

`packet`

Пакет WDDX у вигляді рядка чи потоку.

### Значення, що повертаються

Повертає десеріалізоване значення, яке може бути рядком, числом чи масивом. Зауважте, що структури десеріалізуються в асоціативні масиви.
