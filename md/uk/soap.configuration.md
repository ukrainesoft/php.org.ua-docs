---
navigation:
  - soap.installation.md: « Встановлення
  - soap.resources.md: Типи ресурсів »
  - index.md: PHP Manual
  - soap.setup.md: Встановлення та налаштування
title: Налаштування під час виконання
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
## Налаштування під час виконання

Поведінка цих функцій залежить від установок у php.ini.

**Опції налаштування SOAP**

| Имя | По умолчанию | Место изменения | Список изменений |
| --- | --- | --- | --- |
| [soap.wsdl\_cache\_enabled](soap.configuration.md#ini.soap.wsdl-cache-enabled) |  | **`INI_ALL`** |  |
| [soap.wsdl\_cache\_dir](soap.configuration.md#ini.soap.wsdl-cache-dir) | /tmp | **`INI_ALL`** |  |
| [soap.wsdl\_cache\_ttl](soap.configuration.md#ini.soap.wsdl-cache-ttl) | 86400 | **`INI_ALL`** |  |
| [soap.wsdl\_cache](soap.configuration.md#ini.soap.wsdl-cache) |  | **`INI_ALL`** |  |
| [soap.wsdl\_cache\_limit](soap.configuration.md#ini.soap.wsdl-cache-limit) | 5 | **`INI_ALL`** |  |

Коротке пояснення конфігураційних директив.

`soap.wsdl_cache_enabled`int

Вмикає або вимикає кешування WSDL.

`soap.wsdl_cache_dir`string

Встановлює шлях до директорії, де модуль SOAP зберігатиме кеш-файли.

`soap.wsdl_cache_ttl`int

Встановлює кількість секунд (час життя) для файлів у кеші, які вони використовуватимуть замість оригінальних файлів.

`soap.wsdl_cache`int

Якщо параметр `soap.wsdl_cache_enabled` набуває значення "on", то ця опція визначає тип кешування. Він може бути будь-яким з наступних типів: **`WSDL_CACHE_NONE`** **`WSDL_CACHE_DISK`** **`WSDL_CACHE_MEMORY`** ) или\*\*`WSDL_CACHE_BOTH`\*\* `3`). Це також може бути встановлене через масив `options` у конструкторі [SoapClient](class.soapclient.md) або [SoapServer](class.soapserver.md)

`soap.wsdl_cache_limit`int

Максимальна кількість кешованих файлів WSDL, що знаходяться в оперативній пам'яті. Подальше додавання файлів у заповнену кеш-пам'ять призведе до видалення з неї найстаріших файлів.
