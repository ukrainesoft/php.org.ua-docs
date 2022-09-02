---
navigation:
  - ref.session.md: « Функції для роботи з сесіями
  - function.session-cache-expire.md: sessioncacheexpire »
  - index.md: PHP Manual
  - ref.session.md: Функції для роботи із сесіями
title: sessionabort
---
# sessionabort

(PHP 5> = 5.6.0, PHP 7, PHP 8)

sessionabort — Скасує зміни в масиві сесії та завершує її

### Опис

```methodsynopsis
session_abort(): bool
```

**sessionabort()** завершує сесію без збереження даних. Отже, зберігаються вихідні значення сесії.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | Тепер тип цієї функції bool, що повертається. Раніше був тип void. |

### Дивіться також

-   [SESSION](reserved.variables.session.md)
-   Директива конфігурації [session.autostart](session.configuration.md#ini.session.auto-start)
-   [sessionstart()](function.session-start.md) - Стартує нову сесію, або відновлює існуючу
-   [sessionreset()](function.session-reset.md) - реініціалізує сесію оригінальними значеннями
-   [sessioncommit()](function.session-commit.md) - Псевдонім sessionwriteclose
