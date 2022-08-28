Встановлює розмір та усунення об'єкта Imagick

-   [« Imagick::setSize](imagick.setsize.html)
    
-   [Imagick::setType »](imagick.settype.html)
    
-   [PHP Manual](index.html)
    
-   [Imagick](class.imagick.html)
    
-   Встановлює розмір та усунення об'єкта Imagick
    

# Imagick::setSizeOffset

(PECL imagick 2, PECL imagick 3)

Imagick::setSizeOffset — Встановлює розмір та усунення об'єкта Imagick

### Опис

```methodsynopsis
public Imagick::setSizeOffset(int $columns, int $rows, int $offset): bool
```

Встановлює розмір та усунення об'єкта Imagick. Встановіть його перед читанням необробленого формату зображення, як RGB, GRAY або CMYK. Цей метод доступний, якщо Imagick був скомпільований з версією ImageMagick 6.2.9 або старшим.

### Список параметрів

`columns`

Ширина у пікселях.

`rows`

Висота у пікселях.

`offset`

Зміщення зображення.

### Значення, що повертаються

У разі успішної роботи повертає **`true`**