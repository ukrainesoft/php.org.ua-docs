---
navigation:
  - function.ob-get-status.md: « ob\_get\_status
  - function.ob-list-handlers.md: ob\_list\_handlers »
  - index.md: PHP Manual
  - ref.outcontrol.md: Функції контролю виведення
title: ob\_implicit\_flush
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ob\_implicit\_flush

(PHP 4, PHP 5, PHP 7, PHP 8)

ob\_implicit\_flush — Вмикає/вимикає неявне скидання

### Опис

```methodsynopsis
ob_implicit_flush(bool $enable = true): void
```

Функция**ob\_implicit\_flush()** включає або вимикає неявне скидання. Неявне скидання призведе до операції скидання після кожного блоку коду, який виводить дані, тому явні виклики функції [flush()](function.flush.md) більше не будуть потрібні.

> **Зауваження**: Друк порожніх рядків або надсилання заголовків не розглядаються як висновок та не скидають висновок.

> **Зауваження**: Ця функція не впливає на обробники виведення рівня користувача, наприклад ті, які запускаються функцією [ob\_start()](function.ob-start.md) або [output\_add\_rewrite\_var()](function.output-add-rewrite-var.md)

### Список параметрів

`enable`

Значение\*\*`true`\*\* включає неявне скидання, а значення **`false`** - відключає.

### Значення, що повертаються

Функція не повертає значення після виконання.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | Тепер параметр `enable` набуває логічного значення (bool); раніше приймалося ціле число (int). |

### Дивіться також

-   [flush()](function.flush.md) \- скидає системний буфер виводу
-   [ob\_start()](function.ob-start.md) \- Включає буферизацію виводу
-   [ob\_end\_flush()](function.ob-end-flush.md) \- Скидає (відправляє) значення активного оброблювача виводу, що повертається, і відключає активний буфер виводу
