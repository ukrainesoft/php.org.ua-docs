---
navigation:
  - function.session-register-shutdown.md: « sessionregistershutdown
  - function.session-save-path.md: sessionsavepath »
  - index.md: PHP Manual
  - ref.session.md: Функції для роботи із сесіями
title: sessionreset
---
# sessionreset

(PHP 5> = 5.6.0, PHP 7, PHP 8)

sessionreset - Реініціалізує сесію оригінальними значеннями

### Опис

```methodsynopsis
session_reset(): bool
```

Функція **sessionreset()** повторно ініціалізує сесію, використовуючи оригінальні значення, збережені у сховищі сесії. Ця функція вимагає наявності активної сесії та знищує всі зміни в масиві $SESSION.

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
-   Опція конфігурації [session.autostart](session.configuration.md#ini.session.auto-start)
-   [sessionstart()](function.session-start.md) - Стартує нову сесію, або відновлює існуючу
-   [sessionabort()](function.session-abort.md) - Скасує зміни у масиві сесії та завершує її
-   [sessioncommit()](function.session-commit.md) - Псевдонім sessionwriteclose
