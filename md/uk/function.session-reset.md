Реініціалізує сесію оригінальними значеннями

-   [« session\_register\_shutdown](function.session-register-shutdown.html)
    
-   [session\_save\_path »](function.session-save-path.html)
    
-   [PHP Manual](index.html)
    
-   [Функции для работы с сессиями](ref.session.html)
    
-   Реініціалізує сесію оригінальними значеннями
    

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

| Версия | Описание                                                           |
|--------|--------------------------------------------------------------------|
|        | Тепер тип цієї функції bool, що повертається. Раніше був тип void. |

### Дивіться також

-   [$\_SESSION](reserved.variables.session.html)
-   Опція конфігурації [session.auto\_start](session.configuration.html#ini.session.auto-start)
-   [session\_start()](function.session-start.html) - Стартує нову сесію, або відновлює існуючу
-   [session\_abort()](function.session-abort.html) - Скасує зміни у масиві сесії та завершує її
-   [session\_commit()](function.session-commit.html) - Псевдонім sessionwriteclose