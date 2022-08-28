Налаштування під час виконання

-   [« Установка](imagick.installation.html)
    
-   [Типы ресурсов »](imagick.resources.html)
    
-   [PHP Manual](index.html)
    
-   [Установка и настройка](imagick.setup.html)
    
-   Налаштування під час виконання
    

## Налаштування під час виконання

Поведінка цих функцій залежить від установок у php.ini.

**Конфігураційні опції Imagick**

| Имя | По умолчанию | Место изменения | Список изменений |
| --- | --- | --- | --- |
| [imagick.locale\_fix](imagick.configuration.html#ini.imagick.locale-fix) | **`false`** | PHPINIALL | Доступно з Imagick 2.1.0 |
| [imagick.progress\_monitor](imagick.configuration.html#ini.imagick.progress-monitor) | **`false`** | PHPINISYSTEM | Доступно з Imagick 2.2.2 |
| [imagick.skip\_version\_check](imagick.configuration.html#ini.imagick.skip-version-check) | **`false`** | PHPINISYSTEM | Доступно з Imagick 3.3.0 |

Для детального опису констант PHPINI, зверніться до розділу [Где могут быть установлены параметры конфигурации](configuration.changes.modes.html)

Коротке пояснення конфігураційних директив.

`imagick.locale_fix` bool

Виправлення помилки малювання з локаллю, використовуючи '`,`' як роздільник.

`imagick.progress_monitor` bool

Використовується для увімкнення моніторингу прогресу.

`imagick.skip_version_check` bool

Коли Imagic завантажений, він перевіряє, що версія ImageMagick, з якою він був скомпільований, збігається з поточною версією і, якщо не збігається, виводить попередження. Це попередження можна придушити, встановивши цей параметр.

Використовувати Imagic із версією ImageMagick відмінною від тієї, з якою він був скомпільований, не рекомендується. Він може працювати, а може завершуватися аварійно, або поводитись непередбачено.