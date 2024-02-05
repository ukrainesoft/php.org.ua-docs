---
navigation:
  - ffi.installation.md: « Встановлення
  - ffi.resources.md: Типи ресурсів »
  - index.md: PHP Manual
  - ffi.setup.md: Встановлення та налаштування
title: Налаштування під час виконання
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
## Налаштування під час виконання

Поведінка цих функцій залежить від установок у php.ini.

**Опції налаштування FFI**

| Имя | По умолчанию | Место изменения | Список изменений |
| --- | --- | --- | --- |
| [ffi.enable](ffi.configuration.md#ini.ffi.enable) | "preload" | **`INI_SYSTEM`** |  |
| [ffi.preload](ffi.configuration.md#ini.ffi.preload) | "" | **`INI_SYSTEM`** |  |

Додаткова інформація та опис режимів INI\_\* дано у розділі «[Місця встановлення параметрів конфігурації](configuration.changes.modes.md)».

Коротке пояснення конфігураційних директив.

`ffi.enable`string

Дозволяє дозволити (`"true"`) або заборонити (`"false"`) використання FFI API, або обмежити використання тільки для CLI SAPI та передзавантажених файлів (`"preload"`

Обмеження FFI API впливають лише на клас [FFI](class.ffi.md), але не на перезавантажені функції об'єкта [FFI\\CData](class.ffi-cdata.md). Це означає, що можна створити об'єкти [FFI\\CData](class.ffi-cdata.md) в передзавантажуваних файлах і потім використовувати безпосередньо зі скриптів PHP.

`ffi.preload`string

Дозволяє завантажувати прив'язки FFI під час старту, що неможливо з [FFI::load()](ffi.load.md), якщо увімкнено [opcache.preload\_user](opcache.configuration.md#ini.opcache.preload-user). Ця директива приймає список роздільників імен файлів **`DIRECTORY_SEPARATOR`**. Передзавантажені прив'язки доступні за допомогою дзвінка [FFI::scope()](ffi.scope.md)
