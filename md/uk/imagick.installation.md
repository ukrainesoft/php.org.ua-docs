---
navigation:
  - imagick.requirements.md: « Вимоги
  - imagick.configuration.md: Налаштування під час виконання »
  - index.md: PHP Manual
  - imagick.setup.md: Встановлення та налаштування
title: Установка
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
## Установка

Цей модуль [» PECL](https://pecl.php.net/)не поставляется вместе с PHP.

Інформація щодо встановлення цього модуля PECL може бути знайдена у розділі посібника [Встановлення PECL модулів](install.pecl.md). Додаткову інформацію, таку як нові версії, завантаження, вихідні файли, інформація про розробника та CHANGELOG, можна знайти тут: [» https://pecl.php.net/package/imagick](https://pecl.php.net/package/imagick)

> **Зауваження**: Офіційна назва цього модуля - *imagick*

Користувачі Windows можуть завантажити готовий файл DLL зі сторінки [» PECL](https://windows.php.net/downloads/pecl/releases/imagick). Ці пакети містять DLL-модуль (php\_imagick.dll), який необхідно помістити в [extension\_dir](ini.core.md#ini.extension-dir). Вони також містять DLL-бібліотеки ImageMagick, які необхідно помістити десь у PATH. Починаючи з Imagick 3.6.0, вони також містять конфігураційні файли XML в config; щоб використовувати їх замість вбудованих значень за умовчанням, їх необхідно помістити в `%USERPROFILE%/.config/ImageMagick` або, натомість по шляху, заданому в змінній оточенні MAGICK\_CONFIGURE\_PATH. Додаткові відомості дивіться у [» документації щодо файлів конфігурації ImageMagick](http://www.imagemagick.org/script/resources.php)
