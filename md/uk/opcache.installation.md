- [« Вимоги](opcache.requirements.md)
- [Налаштування під час виконання »](opcache.configuration.md)

- [PHP Manual](index.md)
- [Встановлення та налаштування](opcache.setup.md)
- Встановлення

## Установка

OPcache можна збирати тільки як модуль, що розділяється. Якщо ви заборонили
збирання модулів за замовчуванням за допомогою **--disable-all**, то вам буде
необхідно компілювати PHP з ключем ** --enable-opcache** для включення
OPcache.

Один раз скомпілювавши, ви можете використовувати директиву конфігурації
[zend_extension](ini.core.md#ini.zend-extension) для завантаження OPcache
у PHP. Це можна зробити за допомогою
`zend_extension=/full/path/to/opcache.so` для платформ, відмінних від
Windows, і `zend_extension=C:\path o\php_opcache.dll` у Windows.

> **Примітка**:
>
> Якщо ви хочете використовувати OPcache з [»Xdebug](http://xdebug.org/),
> спочатку потрібно завантажувати OPcache, а потім Xdebug.

### Рекомендовані налаштування php.ini

Дані опції рекомендовані для забезпечення хорошої продуктивності:

opcache.memory_consumption=128
opcache.interned_strings_buffer=8
opcache.max_accelerated_files=4000
opcache.revalidate_freq=60
opcache.fast_shutdown=1
opcache.enable_cli=1

Ви також можете розглянути можливість відключення
[opcache.save_comments](opcache.configuration.md#ini.opcache.save-comments)
та включення
[opcache.enable_file_override](opcache.configuration.md#ini.opcache.enable-file-override).
Однак, зверніть увагу, що вам доведеться протестувати свій код,
перш ніж використовувати його в промисловій експлуатації, так як відомі
випадки, коли деякі фреймворки та програми переставали працювати,
особливо у разі використання анотацій у коментарях.

У Windows має бути включений параметр
[opcache.file_cache_fallback](opcache.configuration.md#ini.opcache.file-cache-fallback)
і
[opcache.file_cache](opcache.configuration.md#ini.opcache.file-cache)
має бути встановлена на вже існуючий та доступний для запису
каталог.

Повний список опцій налаштування OPcache [дивіться тут](opcache.configuration.md).
