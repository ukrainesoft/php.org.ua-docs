Шифрує зображення

-   [« Imagick::embossImage](imagick.embossimage.html)
    
-   [Imagick::enhanceImage »](imagick.enhanceimage.html)
    
-   [PHP Manual](index.html)
    
-   [Imagick](class.imagick.html)
    
-   Шифрує зображення
    

# Imagick::encipherImage

(PECL imagick 2> = 2.3.0, PECL imagick 3)

Imagick::encipherImage — Шифрує зображення

### Опис

```methodsynopsis
public Imagick::encipherImage(string $passphrase): bool
```

Перетворює звичайні пікселі на зашифровані пікселі. Зображення не читається, доки не буде розшифровано за допомогою [Imagick::decipherImage()](imagick.decipherimage.html) Цей метод доступний, якщо Imagick був скомпільований з версією ImageMagick 6.3.9 або старшим.

### Список параметрів

`passphrase`

Пароль

### Значення, що повертаються

У разі успішної роботи повертає **`true`**

### Дивіться також

-   [Imagick::decipherImage()](imagick.decipherimage.html) - Розшифровує зображення