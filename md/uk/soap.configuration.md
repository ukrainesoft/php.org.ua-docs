Налаштування під час виконання

-   [« Установка](soap.installation.html)
    
-   [Типы ресурсов »](soap.resources.html)
    
-   [PHP Manual](index.html)
    
-   [Установка и настройка](soap.setup.html)
    
-   Налаштування під час виконання
    

## Налаштування під час виконання

Поведінка цих функцій залежить від установок у php.ini.

**Опції налаштування SOAP**

| Имя | По умолчанию | Место изменения | Список изменений |
| --- | --- | --- | --- |
| [soap.wsdl\_cache\_enabled](soap.configuration.html#ini.soap.wsdl-cache-enabled) |  | PHPINIALL |  |
| [soap.wsdl\_cache\_dir](soap.configuration.html#ini.soap.wsdl-cache-dir) | /tmp | PHPINIALL |  |
| [soap.wsdl\_cache\_ttl](soap.configuration.html#ini.soap.wsdl-cache-ttl) |  | PHPINIALL |  |
| [soap.wsdl\_cache](soap.configuration.html#ini.soap.wsdl-cache) |  | PHPINIALL |  |
| [soap.wsdl\_cache\_limit](soap.configuration.html#ini.soap.wsdl-cache-limit) |  | PHPINIALL |  |

Коротке пояснення конфігураційних директив.

`soap.wsdl_cache_enabled` int

Вмикає або вимикає кешування WSDL.

`soap.wsdl_cache_dir` string

Встановлює шлях до директорії, де модуль SOAP зберігатиме кеш-файли.

`soap.wsdl_cache_ttl` int

Встановлює кількість секунд (час життя) для файлів у кеші, які вони використовуватимуть замість оригінальних файлів.

`soap.wsdl_cache` int

Якщо параметр `soap.wsdl_cache_enabled` набуває значення "on", то ця опція визначає тип кешування. Він може бути будь-яким з наступних типів: **`WSDL_CACHE_NONE`** `0` **`WSDL_CACHE_DISK`** `1` **`WSDL_CACHE_MEMORY`** `2`) або **`WSDL_CACHE_BOTH`** `3`). Це також може бути встановлене через масив `options` у конструкторі [SoapClient](class.soapclient.html) або [SoapServer](class.soapserver.html)

`soap.wsdl_cache_limit` int

Максимальна кількість кешованих файлів WSDL, що знаходяться в оперативній пам'яті. Подальше додавання файлів у заповнену кеш-пам'ять призведе до видалення з неї найстаріших файлів.