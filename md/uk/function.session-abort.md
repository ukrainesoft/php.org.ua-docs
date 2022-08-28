Скасовує зміни у масиві сесії та завершує її

-   [« Функции для работы с сессиями](ref.session.html)
    
-   [session\_cache\_expire »](function.session-cache-expire.html)
    
-   [PHP Manual](index.html)
    
-   [Функции для работы с сессиями](ref.session.html)
    
-   Скасовує зміни у масиві сесії та завершує її
    

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

| Версия | Описание                                                           |
|--------|--------------------------------------------------------------------|
|        | Тепер тип цієї функції bool, що повертається. Раніше був тип void. |

### Дивіться також

-   [$\_SESSION](reserved.variables.session.html)
-   Директива конфігурації [session.auto\_start](session.configuration.html#ini.session.auto-start)
-   [session\_start()](function.session-start.html) - Стартує нову сесію, або відновлює існуючу
-   [session\_reset()](function.session-reset.html) - реініціалізує сесію оригінальними значеннями
-   [session\_commit()](function.session-commit.html) - Псевдонім sessionwriteclose