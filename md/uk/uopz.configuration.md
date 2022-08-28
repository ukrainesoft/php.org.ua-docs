Налаштування під час виконання

-   [« Установка](uopz.installation.html)
    
-   [Типы ресурсов »](uopz.resources.html)
    
-   [PHP Manual](index.html)
    
-   [Установка и настройка](uopz.setup.html)
    
-   Налаштування під час виконання
    

## Налаштування під час виконання

Поведінка цих функцій залежить від установок у php.ini.

**uopz Опції налаштування**

| Имя | По умолчанию | Место изменения | Список изменений |
| --- | --- | --- | --- |
| [uopz.disable](uopz.configuration.html#ini.uopz.disable) | "0" | PHPINISYSTEM | Доступно з uopz 5.0.2 |
| [uopz.exit](uopz.configuration.html#ini.uopz.exit) | "0" | PHPINISYSTEM | Доступно з uopz 6.0.1 |
| [uopz.overloads](uopz.configuration.html#ini.uopz.overloads) | "1" | PHPINISYSTEM | Доступно з uopz 2.0.2. Видалено з uopz 5.0.0. |

Для детального опису констант PHPINI, зверніться до розділу [Где могут быть установлены параметры конфигурации](configuration.changes.modes.html)

Коротке пояснення конфігураційних директив.

`uopz.disable` bool

Якщо увімкнено, uopz перестане впливати на роботу PHP.

`uopz.exit` bool

Чи дозволяти модулю виконувати опкод exit (вихід). Ця установка може бути перевизначена під час виконання за допомогою функції [uopz\_allow\_exit()](function.uopz-allow-exit.html)

`uopz.overloads` bool

Дає можливість використовувати [uopz\_overload()](function.uopz-overload.html)

> **Зауваження**: Під час роботи з увімкненим OPcache може знадобитися вимкнути все [оптимизации OPcache](opcache.configuration.html#ini.opcache.optimization-level) `opcache.optimization_level=0`