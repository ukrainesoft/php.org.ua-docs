Скасовує зміни у масиві сесії та завершує її

-   [« Функції для роботи з сесіями](ref.session.md)
    
-   [sessioncacheexpire »](function.session-cache-expire.html)
    
-   [PHP Manual](index.md)
    
-   [Функції для роботи із сесіями](ref.session.md)
    
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

-   [SESSION](reserved.variables.session.md)
-   Директива конфігурації [session.autostart](session.configuration.html#ini.session.auto-start)
-   [sessionstart()](function.session-start.html) - Стартує нову сесію, або відновлює існуючу
-   [sessionreset()](function.session-reset.html) - реініціалізує сесію оригінальними значеннями
-   [sessioncommit()](function.session-commit.html) - Псевдонім sessionwriteclose