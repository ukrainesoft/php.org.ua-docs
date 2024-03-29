---
navigation:
  - opcache.requirements.md: « Вимоги
  - opcache.configuration.md: Налаштування під час виконання »
  - index.md: PHP Manual
  - opcache.setup.md: Встановлення та налаштування
title: Установка
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
## Установка

OPcache можна збирати тільки як модуль, що розділяється. Якщо ви заборонили збирання модулів за замовчуванням за допомогою **\--disable-all**, то вам буде необхідно компілювати PHP з ключем **\--enable-opcache**для включения OPcache.

Якось скомпілювавши, ви можете використовувати директиву конфігурації [zend\_extension](ini.core.md#ini.zend-extension) для завантаження OPcache у PHP. Це можна зробити за допомогою `zend_extension=/full/path/to/opcache.so` для платформ, відмінних від Windows, та `zend_extension=C:\path\to\php_opcache.dll`в Windows.

> **Зауваження** :
> 
> Якщо ви хочете використовувати OPcache з [» Xdebug](http://xdebug.org/), то спочатку потрібно завантажувати OPcache, а потім Xdebug.

### Рекомендовані налаштування php.ini

Дані опції рекомендовані для забезпечення хорошої продуктивності:

```
opcache.memory_consumption=128
opcache.interned_strings_buffer=8
opcache.max_accelerated_files=4000
opcache.revalidate_freq=60
opcache.fast_shutdown=1 ; до PHP 7.2.0
opcache.enable_cli=1
```

Ви також можете розглянути можливість відключення [opcache.save\_comments](opcache.configuration.md#ini.opcache.save-comments)и включения[opcache.enable\_file\_override](opcache.configuration.md#ini.opcache.enable-file-override). Однак зверніть увагу, що вам доведеться протестувати свій код, перш ніж використовувати його в промисловій експлуатації, оскільки відомі випадки, коли деякі фреймворки та програми переставали працювати, особливо у разі використання анотацій у коментарях.

У Windows має бути включений параметр [opcache.file\_cache\_fallback](opcache.configuration.md#ini.opcache.file-cache-fallback) і [opcache.file\_cache](opcache.configuration.md#ini.opcache.file-cache) має бути встановлена ​​на вже існуючий та доступний для запису каталог.

Повний список опцій налаштування OPcache [дивіться тут](opcache.configuration.md)
