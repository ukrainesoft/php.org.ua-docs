Записує зображення за вказаним ім'ям файлу

-   [« Imagick::whiteThresholdImage](imagick.whitethresholdimage.html)
    
-   [Imagick::writeImageFile »](imagick.writeimagefile.html)
    
-   [PHP Manual](index.html)
    
-   [Imagick](class.imagick.html)
    
-   Записує зображення за вказаним ім'ям файлу
    

# Imagick::writeImage

(PECL imagick 2> = 2.3.0, PECL imagick 3)

Imagick::writeImage — Записує зображення за вказаним ім'ям файлу

### Опис

```methodsynopsis
public Imagick::writeImage(string $filename = NULL): bool
```

Записує зображення у вказане ім'я файлу. Якщо параметр імені файлу дорівнює NULL, зображення записується в ім'я файлу, встановлене за допомогою Imagick::readImage() або Imagick::setImageFilename().

### Список параметрів

`filename`

Назва файлу, куди записати зображення. Розширення імені файлу визначає тип файлу. Формат може бути примусово встановлений незалежно від розширення файлу, використовуючи префікс "format:", наприклад, "jpg:test.png".

### Значення, що повертаються

У разі успішної роботи повертає **`true`**