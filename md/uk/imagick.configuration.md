---
navigation:
  - imagick.installation.md: « Встановлення
  - imagick.resources.md: Типи ресурсів »
  - index.md: PHP Manual
  - imagick.setup.md: Встановлення та налаштування
title: Налаштування під час виконання
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
## Налаштування під час виконання

Поведінка цих функцій залежить від установок у php.ini.

**Конфігураційні опції Imagick**

| Имя | По умолчанию | Место изменения | Список изменений |
| --- | --- | --- | --- |
| [imagick.locale\_fix](imagick.configuration.md#ini.imagick.locale-fix) | **`false`** | **`INI_ALL`** | Доступно з Imagick 2.1.0 |
| [imagick.progress\_monitor](imagick.configuration.md#ini.imagick.progress-monitor) | **`false`** | **`INI_SYSTEM`** | Доступно з Imagick 2.2.2 |
| [imagick.skip\_version\_check](imagick.configuration.md#ini.imagick.skip-version-check) | **`false`** | **`INI_SYSTEM`** | Доступно з Imagick 3.3.0 |

Додаткова інформація та опис режимів INI\_\* дано у розділі «[Місця встановлення параметрів конфігурації](configuration.changes.modes.md)».

Коротке пояснення конфігураційних директив.

`imagick.locale_fix`bool

Виправлення помилки малювання з локаллю, використовуючи '`,`' як роздільник.

`imagick.progress_monitor`bool

Використовується для активації моніторингу прогресу.

`imagick.skip_version_check`bool

Коли Imagic завантажений, він перевіряє, що версія ImageMagick, з якою він був скомпільований, збігається з поточною версією і, якщо не збігається, виводить попередження. Це попередження можна придушити, встановивши цей параметр.

Використовувати Imagic із версією ImageMagick відмінною від тієї, з якою він був скомпільований, не рекомендується. Він може працювати, а може завершуватися аварійно, або вести себе непередбачено.
