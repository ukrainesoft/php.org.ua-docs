Опис

-   [« Imagick::setProgressMonitor](imagick.setprogressmonitor.html)
    
-   [Imagick::setResolution »](imagick.setresolution.html)
    
-   [PHP Manual](index.html)
    
-   [Imagick](class.imagick.html)
    
-   Опис
    

# Imagick::setRegistry

(PECL imagick 3> = 3.3.0)

Imagick::setRegistry — Опис

### Опис

```methodsynopsis
public static Imagick::setRegistry(string $key, string $value): bool
```

Встановлює запис реєстру ImageMagick з ім'ям key значення. Найкорисніше для встановлення тимчасового шляху, який визначає, де ImageMagick створює тимчасові зображення, наприклад, при обробці PDF-файлів.

### Список параметрів

`key`

`value`

### Значення, що повертаються

У разі успішної роботи повертає **`true`**