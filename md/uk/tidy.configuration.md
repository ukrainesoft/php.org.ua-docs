Налаштування під час виконання

-   [« Установка](tidy.installation.md)
    
-   [Типи ресурсів »](tidy.resources.md)
    
-   [PHP Manual](index.md)
    
-   [Встановлення та налаштування](tidy.setup.md)
    
-   Налаштування під час виконання
    

## Налаштування під час виконання

Поведінка цих функцій залежить від установок у php.ini.

**Параметри конфігурації Tidy**

| Имя | По умолчанию | Место изменения | Список изменений |
| --- | --- | --- | --- |
| [tidy.defaultconfig](tidy.configuration.html#ini.tidy.default-config) | "" | PHPINISYSTEM |  |
| [tidy.cleanoutput](tidy.configuration.html#ini.tidy.clean-output) | "0" | PHPINIUSER |  |

Для детального опису констант PHPINI, зверніться до розділу [Де можуть бути встановлені параметри конфігурації](configuration.changes.modes.md)

Коротке пояснення конфігураційних директив.

`tidy.default_config` string

Шлях за промовчанням до конфігураційного файлу Tidy.

`tidy.clean_output` bool

Вмикає/вимикає відновлення потоку виведення засобами Tidy.

**Увага**

Не слід вмикати `tidy.clean_output` у разі створення контенту, відмінного від html, такого як динамічні зображення.