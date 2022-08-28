Налаштування під час виконання

-   [« Установка](misc.installation.html)
    
-   [Типы ресурсов »](misc.resources.html)
    
-   [PHP Manual](index.html)
    
-   [Установка и настройка](misc.setup.html)
    
-   Налаштування під час виконання
    

## Налаштування під час виконання

Поведінка цих функцій залежить від установок у php.ini.

**Опції налаштувань різних функцій**

| Имя                                                                  | По умолчанию | Место изменения | Список изменений |
|----------------------------------------------------------------------|--------------|-----------------|------------------|
| [ignore\_user\_abort](misc.configuration.html#ini.ignore-user-abort) | "0"          | PHPINIALL       |                  |
| [highlight.string](misc.configuration.html#ini.syntax-highlighting)  | "#DD0000"    | PHPINIALL       |                  |
| [highlight.comment](misc.configuration.html#ini.syntax-highlighting) | "#FF8000"    | PHPINIALL       |                  |
| [highlight.keyword](misc.configuration.html#ini.syntax-highlighting) | "#007700"    | PHPINIALL       |                  |
| [highlight.default](misc.configuration.html#ini.syntax-highlighting) | "#0000BB"    | PHPINIALL       |                  |
| [highlight.html](misc.configuration.html#ini.syntax-highlighting)    | "#000000"    | PHPINIALL       |                  |
| [browscap](misc.configuration.html#ini.browscap)                     | NULL         | PHPINISYSTEM    |                  |

Для детального опису констант PHPINI, зверніться до розділу [Где могут быть установлены параметры конфигурации](configuration.changes.modes.html)

Коротке пояснення конфігураційних директив.

`ignore_user_abort` bool

**`false`** за замовчуванням. Якщо змінюється на **`true`**, Скрипти не будуть перервані після того, як клієнт розірве з'єднання.

Дивіться також [ignore\_user\_abort()](function.ignore-user-abort.html)

`highlight.bg` string

`highlight.comment` string

`highlight.default` string

`highlight.html` string

`highlight.keyword` string

`highlight.string` string

Кольори для режиму підсвічування (Syntax Highlighting). Все, що прийнятно в , буде працювати.

`browscap` string

Ім'я (наприклад, browscap.ini) та розташування файлу можливостей браузера. Дивіться також [get\_browser()](function.get-browser.html)