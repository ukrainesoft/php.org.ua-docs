Налаштування під час виконання

-   [« Установка](taint.installation.html)
    
-   [Типы ресурсов »](taint.resources.html)
    
-   [PHP Manual](index.html)
    
-   [Установка и настройка](taint.setup.html)
    
-   Налаштування під час виконання
    

## Налаштування під час виконання

Поведінка цих функцій залежить від установок у php.ini.

**Опції налаштування Taint**

| Имя                                                                | По умолчанию | Место изменения | Список изменений |
|--------------------------------------------------------------------|--------------|-----------------|------------------|
| [taint.enable](taint.configuration.html#ini.taint.enable)          |              | PHPINISYSTEM    |                  |
| [taint.errorlevel](taint.configuration.html#ini.taint.error-level) | ЕWARNING     | PHPINIALL       |                  |

Коротке пояснення конфігураційних директив.

`taint.enable` int

Чи увімкнено модуль.

`taint.error_level` int

Тип помилки, який повертатиме модуль при виявленні підозрілого рядка.