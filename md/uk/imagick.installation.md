Встановлення

-   [« Требования](imagick.requirements.html)
    
-   [Настройка во время выполнения »](imagick.configuration.html)
    
-   [PHP Manual](index.html)
    
-   [Установка и настройка](imagick.setup.html)
    
-   Встановлення
    

## Встановлення

Цей модуль [» PECL](https://pecl.php.net/) не постачається разом з PHP.

Інформація щодо встановлення цього модуля PECL може бути знайдена у розділі посібника [Установка PECL модулей](install.pecl.html). Додаткову інформацію, таку як нові версії, завантаження, вихідні файли, інформація про розробника та CHANGELOG, можна знайти тут: [» https://pecl.php.net/package/imagick](https://pecl.php.net/package/imagick)

> **Зауваження**: Офіційна назва цього модуля - *imagick*

Користувачі Windows можуть завантажити готовий файл DLL зі сторінки [» PECL](https://windows.php.net/downloads/pecl/releases/imagick). Ці пакети містять DLL-модуль (phpimagick.dll), який необхідно помістити в [extension\_dir](ini.core.html#ini.extension-dir). Вони також містять DLL-бібліотеки ImageMagick, які необхідно помістити десь у PATH. Починаючи з Imagick 3.6.0, вони також містять конфігураційні файли XML в config; щоб використовувати їх замість вбудованих значень за умовчанням, їх необхідно помістити в `%USERPROFILE%/.config/ImageMagick` або, натомість по шляху, заданому в змінній оточенні MAGICKCONFIGUREPATH. Додаткові відомості дивіться у [» документации по файлам конфигурации ImageMagick](http://www.imagemagick.org/script/resources.php)