Налаштування під час виконання

-   [« Установка](imagick.installation.html)
    
-   [Типи ресурсів »](imagick.resources.html)
    
-   [PHP Manual](index.html)
    
-   [Встановлення та налаштування](imagick.setup.html)
    
-   Налаштування під час виконання
    

## Налаштування під час виконання

Поведінка цих функцій залежить від установок у php.ini.

**Конфігураційні опції Imagick**

| Имя | По умолчанию | Место изменения | Список изменений |
| --- | --- | --- | --- |
| [imagick.localefix](imagick.configuration.html#ini.imagick.locale-fix) | **`false`** | PHPINIALL | Доступно з Imagick 2.1.0 |
| [imagick.progressmonitor](imagick.configuration.html#ini.imagick.progress-monitor) | **`false`** | PHPINISYSTEM | Доступно з Imagick 2.2.2 |
| [imagick.skipversioncheck](imagick.configuration.html#ini.imagick.skip-version-check) | **`false`** | PHPINISYSTEM | Доступно з Imagick 3.3.0 |

Для детального опису констант PHPINI, зверніться до розділу [Де можуть бути встановлені параметри конфігурації](configuration.changes.modes.html)

Коротке пояснення конфігураційних директив.

`imagick.locale_fix` bool

Виправлення помилки малювання з локаллю, використовуючи '`,`' як роздільник.

`imagick.progress_monitor` bool

Використовується для увімкнення моніторингу прогресу.

`imagick.skip_version_check` bool

Коли Imagic завантажений, він перевіряє, що версія ImageMagick, з якою він був скомпільований, збігається з поточною версією і, якщо не збігається, виводить попередження. Це попередження можна придушити, встановивши цей параметр.

Використовувати Imagic із версією ImageMagick відмінною від тієї, з якою він був скомпільований, не рекомендується. Він може працювати, а може завершуватися аварійно, або поводитись непередбачено.