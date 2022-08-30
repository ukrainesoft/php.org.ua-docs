Встановлення

-   [« Вимоги](exif.requirements.md)
    
-   [Налаштування під час виконання »](exif.configuration.md)
    
-   [PHP Manual](index.md)
    
-   [Встановлення та налаштування](exif.setup.md)
    
-   Встановлення
    

## Встановлення

Щоб увімкнути підтримку exif, налаштуйте PHP з опцією **\-enable-exif**

Користувачі Windows повинні увімкнути DLL-файли phpmbstring.dll та phpexif.dll у php.ini. DLL phpmbstring.dll повинна бути завантажена *до* DLL phpexif.dll, так що налаштуйте ваш php.ini відповідним чином.