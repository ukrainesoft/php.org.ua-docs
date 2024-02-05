---
navigation:
  - function.pcntl-alarm.md: « pcntl\_alarm
  - function.pcntl-errno.md: pcntl\_errno »
  - index.md: PHP Manual
  - ref.pcntl.md: Функції PCNTL
title: pcntl\_async\_signals
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# pcntl\_async\_signals

(PHP 7 >= 7.1.0, PHP 8)

pcntl\_async\_signals — Увімкнути/вимкнути асинхронну обробку сигналів або отримати поточний статус

### Опис

```methodsynopsis
pcntl_async_signals(?bool $enable = null): bool
```

Якщо пропущено параметр `enable`, функция**pcntl\_async\_signals()** поверне поточне значення налаштування. А якщо заданий, асинхронна обробка буде включена, або відключена, залежно від заданого значення.

### Список параметрів

`enable`

Увімкнути або вимкнути асинхронну обробку сигналів.

### Значення, що повертаються

Если при использовании значение параметра`enable` одно **`null`**, повертає чи включена асинхронна обробка сигналів. Якщо під час використання параметр `enable`не равен\*\*`null`\*\*, повертає, чи була включена асинхронна обробка сигналів *до* виклик функції.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | `enable` тепер допускає значення null. |

### Дивіться також

-   [declare](control-structures.declare.md)
