Налаштування під час виконання

-   [« Установка](uopz.installation.md)
    
-   [Типи ресурсів »](uopz.resources.md)
    
-   [PHP Manual](index.md)
    
-   [Встановлення та налаштування](uopz.setup.md)
    
-   Налаштування під час виконання
    

## Налаштування під час виконання

Поведінка цих функцій залежить від установок у php.ini.

**uopz Опції налаштування**

| Имя                                                          | По умолчанию | Место изменения | Список изменений                              |
|--------------------------------------------------------------|--------------|-----------------|-----------------------------------------------|
| [uopz.disable](uopz.configuration.html#ini.uopz.disable)     | "0"          | PHPINISYSTEM    | Доступно з uopz 5.0.2                         |
| [uopz.exit](uopz.configuration.html#ini.uopz.exit)           | "0"          | PHPINISYSTEM    | Доступно з uopz 6.0.1                         |
| [uopz.overloads](uopz.configuration.html#ini.uopz.overloads) | "1"          | PHPINISYSTEM    | Доступно з uopz 2.0.2. Видалено з uopz 5.0.0. |

Для детального опису констант PHPINI, зверніться до розділу [Де можуть бути встановлені параметри конфігурації](configuration.changes.modes.md)

Коротке пояснення конфігураційних директив.

`uopz.disable` bool

Якщо увімкнено, uopz перестане впливати на роботу PHP.

`uopz.exit` bool

Чи дозволяти модулю виконувати опкод exit (вихід). Ця установка може бути перевизначена під час виконання за допомогою функції [uopzallowexit()](function.uopz-allow-exit.html)

`uopz.overloads` bool

Дає можливість використовувати [uopzoverload()](function.uopz-overload.html)

> **Зауваження**: Під час роботи з увімкненим OPcache може знадобитися вимкнути все [оптимизации OPcache](opcache.configuration.html#ini.opcache.optimization-level) `opcache.optimization_level=0`