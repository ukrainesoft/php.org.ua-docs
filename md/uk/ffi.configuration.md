---
navigation:
  - ffi.installation.md: « Установка
  - ffi.resources.md: Типи ресурсів »
  - index.md: PHP Manual
  - ffi.setup.md: Встановлення та налаштування
title: Налаштування під час виконання
---
## Налаштування під час виконання

Поведінка цих функцій залежить від установок у php.ini.

**Опції налаштування FFI**

| Имя | По умолчанию | Место изменения | Список изменений |
| --- | --- | --- | --- |
| [ffi.enable](ffi.configuration.html#ini.ffi.enable) | "preload" | PHPINISYSTEM |  |
| [ffi.preload](ffi.configuration.html#ini.ffi.preload) | "" | PHPINISYSTEM |  |

Для детального опису констант PHPINI, зверніться до розділу [Де можуть бути встановлені параметри конфігурації](configuration.changes.modes.md)

Коротке пояснення конфігураційних директив.

`ffi.enable` string

Дозволяє дозволити (`"true"`) або заборонити (`"false"`) використання FFI API, або обмежити використання тільки для CLI SAPI та передзавантажених файлів (`"preload"`

Обмеження FFI API впливають лише на клас [FFI](class.ffi.md), але не на перезавантажені функції об'єкта [FFICData](class.ffi-cdata.html). Це означає, що можна створити об'єкти [FFICData](class.ffi-cdata.md) у завантажуваних файлах і використовувати потім безпосередньо зі скриптів PHP.

`ffi.preload` string

Дозволяє завантажувати прив'язки FFI під час старту, що неможливо з [FFI::load()](ffi.load.md), якщо увімкнено [opcache.preloaduser](opcache.configuration.html#ini.opcache.preload-user). Ця директива приймає список роздільників імен файлів **`DIRECTORY_SEPARATOR`**. Передзавантажені прив'язки доступні за допомогою дзвінка [FFI::scope()](ffi.scope.md)
