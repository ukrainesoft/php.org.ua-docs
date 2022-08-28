Розшифровує зображення

-   [« Imagick::cycleColormapImage](imagick.cyclecolormapimage.html)
    
-   [Imagick::deconstructImages »](imagick.deconstructimages.html)
    
-   [PHP Manual](index.html)
    
-   [Imagick](class.imagick.html)
    
-   Розшифровує зображення
    

# Imagick::decipherImage

(PECL imagick 2> = 2.3.0, PECL imagick 3)

Imagick::decipherImage — Розшифровує зображення

### Опис

```methodsynopsis
public Imagick::decipherImage(string $passphrase): bool
```

Розшифровує зображення, яке було зашифровано раніше. Зображення має бути зашифроване з використанням [Imagick::encipherImage()](imagick.encipherimage.html). Цей метод доступний, якщо Imagick був скомпільований з версією ImageMagick 6.3.9 або старшим.

### Список параметрів

`passphrase`

Пароль

### Значення, що повертаються

У разі успішної роботи повертає **`true`**

### Дивіться також

-   [Imagick::encipherImage()](imagick.encipherimage.html) - Шифрує зображення