Налаштування під час виконання

-   [« Установка](ffi.installation.html)
    
-   [Типы ресурсов »](ffi.resources.html)
    
-   [PHP Manual](index.html)
    
-   [Установка и настройка](ffi.setup.html)
    
-   Налаштування під час виконання
    

## Налаштування під час виконання

Поведінка цих функцій залежить від установок у php.ini.

**Опції налаштування FFI**

| Имя                                                   | По умолчанию | Место изменения | Список изменений |
|-------------------------------------------------------|--------------|-----------------|------------------|
| [ffi.enable](ffi.configuration.html#ini.ffi.enable)   | "preload"    | PHPINISYSTEM    |                  |
| [ffi.preload](ffi.configuration.html#ini.ffi.preload) | ""           | PHPINISYSTEM    |                  |

Для детального опису констант PHPINI, зверніться до розділу [Где могут быть установлены параметры конфигурации](configuration.changes.modes.html)

Коротке пояснення конфігураційних директив.

`ffi.enable` string

Дозволяє дозволити (`"true"`) або заборонити (`"false"`) використання FFI API, або обмежити використання тільки для CLI SAPI та передзавантажених файлів (`"preload"`

Обмеження FFI API впливають лише на клас [FFI](class.ffi.html), але не на перезавантажені функції об'єкта [FFI\\CData](class.ffi-cdata.html). Це означає, що можна створити об'єкти [FFI\\CData](class.ffi-cdata.html) у завантажуваних файлах і використовувати потім безпосередньо зі скриптів PHP.

`ffi.preload` string

Дозволяє завантажувати прив'язки FFI під час старту, що неможливо з [FFI::load()](ffi.load.html), якщо увімкнено [opcache.preload\_user](opcache.configuration.html#ini.opcache.preload-user). Ця директива приймає список роздільників імен файлів **`DIRECTORY_SEPARATOR`**. Передзавантажені прив'язки доступні за допомогою дзвінка [FFI::scope()](ffi.scope.html)