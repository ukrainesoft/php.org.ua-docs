- [« Установка](imagick.installation.md)
- [Типи ресурсів»](imagick.resources.md)

- [PHP Manual](index.md)
- [Встановлення та налаштування](imagick.setup.md)
- Налаштування під час виконання

## Налаштування під час виконання

Поведінка цих функцій залежить від установок `php.ini`.

| Ім'я За замовчуванням                                                                 | Місце зміни | Список змін    |
| ------------------------------------------------------------------------------------- | ----------- | -------------- |
| [imagick.locale_fix](imagick.configuration.md#ini.imagick.locale-fix)                 | **false**   | PHP_INI_ALL    | Доступно з Imagick 2.1.0 |                
| [imagick.progress_monitor](imagick.configuration.md#ini.imagick.progress-monitor)     | **false**   | PHP_INI_SYSTEM | Доступно з Imagick 2.2.2
| [imagick.skip_version_check](imagick.configuration.md#ini.imagick.skip-version-check) | **false**   | PHP_INI_SYSTEM | Доступно з Imagick 3.3.0

**Конфігураційні опції Imagick**

Для детального опису констант PHP_INI\_\*, зверніться до розділу [Де
можуть бути встановлені параметри конфігурації](configuration.changes.modes.md).

Коротке пояснення конфігураційних директив.

`imagick.locale_fix` bool
Виправлення помилки малювання з локаллю, використовуючи '','' як
роздільника.

`imagick.progress_monitor` bool
Використовується для активації моніторингу прогресу.

`imagick.skip_version_check` bool
Коли Imagic завантажений, він перевіряє, що версія ImageMagick, з якою
він був скомпільований, збігається з поточною версією, що використовується і, якщо
не збігається, виводить попередження. Це попередження можна придушити,
встановивши цей параметр.

Використовувати Imagic із версією ImageMagick відмінною від тієї, з якою він
був скомпільований, не рекомендується. Він може працювати, а може
завершуватися аварійно, або вести себе непередбачено.
