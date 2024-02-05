---
navigation:
  - ref.session.md: « Функції для роботи з сесіями
  - function.session-cache-expire.md: session\_cache\_expire »
  - index.md: PHP Manual
  - ref.session.md: Функції для роботи із сесіями
title: session\_abort
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# session\_abort

(PHP 5 >= 5.6.0, PHP 7, PHP 8)

session\_abort — Скасує зміни в масиві сесії та завершує її

### Опис

```methodsynopsis
session_abort(): bool
```

**session\_abort()** завершує сесію без збереження даних. Отже, зберігаються вихідні значення сесії.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 7.2.0 | Тепер тип цієї функції bool, що повертається. Раніше був тип void. |

### Дивіться також

-   [$\_SESSION](reserved.variables.session.md)
-   Директива конфігурації[session.auto\_start](session.configuration.md#ini.session.auto-start)
-   [session\_start()](function.session-start.md) \- Стартує нову сесію, або відновлює існуючу
-   [session\_reset()](function.session-reset.md) \- реініціалізує сесію оригінальними значеннями
-   [session\_commit()](function.session-commit.md) \- Псевдонім session\_write\_close
