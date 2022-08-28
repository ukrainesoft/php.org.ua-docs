Вимоги

-   [« Установка и настройка](exif.setup.html)
    
-   [Установка »](exif.installation.html)
    
-   [PHP Manual](index.html)
    
-   [Установка и настройка](exif.setup.html)
    
-   Вимоги
    

## Вимоги

Ваш PHP має бути скомпільований з опцією `--enable-exif`. Для включення підтримки багатобайтових кодувань у тегах EXIF ​​необхідно увімкнути модуль [mbstring](ref.mbstring.html). Включити його можна, скомпілювавши PHP з опцією `--enable-mbstring`

Тільки для Windows: модуль [mbstring](ref.mbstring.html) завжди має бути включений. Зверніть увагу, що модуль [mbstring](ref.mbstring.html) повинен завантажуватись раніше, ніж EXIF ​​(черговість у php.ini).