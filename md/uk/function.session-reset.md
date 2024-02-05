---
navigation:
  - function.session-register-shutdown.md: « session\_register\_shutdown
  - function.session-save-path.md: session\_save\_path »
  - index.md: PHP Manual
  - ref.session.md: Функції для роботи із сесіями
title: session\_reset
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# session\_reset

(PHP 5 >= 5.6.0, PHP 7, PHP 8)

session\_reset - Реініціалізує сесію оригінальними значеннями

### Опис

```methodsynopsis
session_reset(): bool
```

Функция**session\_reset()** повторно ініціалізує сесію, використовуючи оригінальні значення, збережені у сховищі сесії. Ця функція вимагає наявності активної сесії та знищує всі зміни в масиві $\_SESSION.

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
-   Опція конфігурації [session.auto\_start](session.configuration.md#ini.session.auto-start)
-   [session\_start()](function.session-start.md) \- Стартує нову сесію, або відновлює існуючу
-   [session\_abort()](function.session-abort.md) \- Скасує зміни у масиві сесії та завершує її
-   [session\_commit()](function.session-commit.md) \- Псевдонім session\_write\_close
